PHP���ģʽ�ʼǣ�ʹ��PHPʵ�ֺϳ�ģʽ

����ͼ��
��������ϳ����νṹ�Ա�ʾ������-���塱�Ĳ�νṹ��Compositeʹ�û��Ե����������϶����ʹ�þ���һ���ԡ�
Composite�仯����һ������Ľṹ�����

���ϳ�ģʽ����Ҫ��ɫ��
�������(Component)��ɫ�������ɫ�����μ���ϵĶ���涨һ���ӿڡ����ʵ�������£�ʵ�������๲�нӿڵ�ȱʡ��Ϊ������һ���ӿ����ڷ��ʺ͹���Component�������
��Ҷ���(Leaf)��ɫ��������б�ʾҶ�ڵ����Ҷ�ڵ�û���ӽڵ㡣������ж���ͼԪ�������Ϊ��
��֦���(Composite)��ɫ���洢�Ӳ������������Ӳ�������Щ��������Ϊ����Component�ӿ���ʵ�����Ӳ����йصĲ�����
�ͻ���(Client)��ͨ��Component�ӿڲ�����ϲ����Ķ���

���ϳ�ģʽ���ŵ��ȱ�㡿
Compositeģʽ���ŵ�
1���򻯿ͻ�����
2��ʹ�ø��������������͵����

Compositeģʽ��ȱ�㣺ʹ�����Ʊ�ø���һ�㻯�������������Ҳ�����һЩ���⣬�Ǿ��Ǻ�����������е����

���ϳ�ģʽ���ó�����
1�������ʾ����Ĳ���-�����νṹ
2����ϣ���û�������϶���͵�������Ĳ�ͬ���û���ͳһ��ʹ����Ͻṹ�е����ж���

���ϳ�ģʽ������ģʽ��
װ����ģʽ��Decoratorģʽ������Compositeģʽһ��ʹ�á���װ����ϳ�һ��ʹ��ʱ������ͨ����һ�������ĸ��ࡣ���װ�α���֧�־���add,remove��getChild������Component�ӿ�
��Ԫģʽ��Flyweightģʽ���㹲��������������������ǵĸ�����
������ģʽ��Itertor����������Composite
������ģʽ��Visitor������Ӧ�÷ֲ���Composite��Leaf���еĲ�������Ϊ�ֲ�����

����ȫʽ�ĺϳ�ģʽ��
��Composite�������������е����������������ķ����������������ǰ�ȫ�ġ���Ϊ��Ҷ���͵Ķ��������û�й�������ķ�������ˣ�����ͻ��˶���Ҷ�����ʹ����Щ����ʱ��������ڱ���ʱ�ڳ�������ͨ�������Ͳ����������ʱ�ڴ���
������ȱ���ǲ���͸������Ϊ��Ҷ��ͺϳ��ཫ���в�ͬ�Ľӿڡ�

����ȫʽ�ĺϳ�ģʽ�ṹͼ��

��ȫʽ�ĺϳ�ģʽ
����ȫʽ�ĺϳ�ģʽPHPʾ����
<?php 
/**
 * �ϳ�ģʽ 2015-10-09
 * 1.Ŀ��
 * ��������ϳ����νṹ�Ա�ʾ������-���塱�Ĳ�νṹ��Compositeʹ�û��Ե����������϶����ʹ�þ���һ���ԡ�
 * 2.ʹ�ó���
 * 2.1 �����ʾ����Ĳ���-�����νṹ
 * 2.2 ��ϣ���û�������϶���͵�������Ĳ�ͬ���û���ͳһ��ʹ����Ͻṹ�е����ж���
 */

/**
 * ��ȫ�ĺϳ�ģʽ
 */

/**
 * ���������ɫ
 */
interface Component
{
 
    /**
     * �����Լ���ʵ��
     */
    public function getComposite();
 
    /**
     * ʾ������
     */
    public function operation();
}
 
/**
 * ��֦�����ɫ
 */
class Composite implements Component
{
    private $_composites;
 
    public function __construct()
    {
        $this->_composites = array();
    }
 
    public function getComposite()
    {
        return $this;
    }
 
    /**
     * ʾ�����������ø����Ӷ����operation����
     */
    public function operation() 
    {
        echo 'Composite operation begin:<br />';
        foreach ($this->_composites as $composite)
        {
            $composite->operation();
        }
        echo 'Composite operation end:<br /><br />';
    }
 
    /**
     * �ۼ������� ���һ���Ӷ���
     * @param Component $component  �Ӷ���
     */
    public function add(Component $component) 
    {
        $this->_composites[] = $component;
    }
 
    /**
     * �ۼ������� ɾ��һ���Ӷ���
     * @param Component $component  �Ӷ���
     * @return boolean  ɾ���Ƿ�ɹ�
     */
    public function remove(Component $component) 
    {
        foreach ($this->_composites as $key => $row) {
            if ($component == $row) {
                unset($this->_composites[$key]);
                return TRUE;
            }
        } 
        return FALSE;
    }
 
    /**
     * �ۼ������� �������е��Ӷ���
     */
    public function getChild() 
    {
       return $this->_composites;
    }
 
}
 
class Leaf implements Component 
{
    private $_name;
 
    public function __construct($name) 
    {
        $this->_name = $name;
    }
 
    public function operation() 
    {
        echo 'Leaf operation ', $this->_name, '<br />';
    }
 
    public function getComposite() 
    {
        return null;
    }
}
 
 
/**
 * �ͻ���
 */
class Client 
{
 
    /**
     * Main program.
     */
    public static function main() 
    {
        $leaf1 = new Leaf('first');
        $leaf2 = new Leaf('second');
 
        $composite = new Composite();
        $composite->add($leaf1);
        $composite->add($leaf2);
        $composite->operation();
 
        $composite->remove($leaf2);
        $composite->operation();
    }
 
} 

Client::main();
?>

��͸��ʽ�ĺϳ�ģʽ��
��Composite�������������е����������������ķ��������������Ǻô������е�����඼����ͬ�Ľӿڡ��ڿͻ��˿�������Ҷ��ͺϳ����������������ڽӿڲ������ʧ�ˣ��ͻ��˿���ͬ�ȵĶԴ����еĶ��������͸����ʽ�ĺϳ�ģʽ
ȱ����ǲ�����ȫ����Ϊ��Ҷ�����ͺϳ�������ڱ�������������ġ���Ҷ����󲻿�������һ����εĶ�����˵�������ӻ�ɾ��������û�������ˣ����ڱ����ڼ��ǲ������ģ���ֻ��������ʱ�ڲŻ����

��͸��ʽ�ĺϳ�ģʽ�ṹͼ��

͸��ʽ�ĺϳ�ģʽ
��͸��ʽ�ĺϳ�ģʽPHPʾ����
<?php 
/**
 * ͸���ĺϳ�ģʽ 2010-08-10                                          
 */
  
/**
 * ���������ɫ
 */
interface Component 
{
    /**
     * �����Լ���ʵ��
     */
    public function getComposite();
 
    /**
     * ʾ������
     */
    public function operation();
 
    /**
     * �ۼ������� ���һ���Ӷ���
     * @param Component $component  �Ӷ���
     */
    public function add(Component $component);
 
    /**
     * �ۼ������� ɾ��һ���Ӷ���
     * @param Component $component  �Ӷ���
     * @return boolean  ɾ���Ƿ�ɹ�
     */
    public function remove(Component $component);
 
    /**
     * �ۼ������� �������е��Ӷ���
     */
    public function getChild(); 
}
 
/**
 * ��֦�����ɫ
 */
class Composite implements Component 
{
    private $_composites;
 
    public function __construct() 
    {
        $this->_composites = array();
    }
 
    public function getComposite() 
    {
        return $this;
    }
 
    /**
     * ʾ�����������ø����Ӷ����operation����
     */
    public function operation() 
    {
        echo 'Composite operation begin:<br />';
        foreach ($this->_composites as $composite) {
            $composite->operation();
        }
        echo 'Composite operation end:<br /><br />';
    }
 
    /**
     * �ۼ������� ���һ���Ӷ���
     * @param Component $component  �Ӷ���
     */
    public function add(Component $component) 
    {
        $this->_composites[] = $component;
    }
 
    /**
     * �ۼ������� ɾ��һ���Ӷ���
     * @param Component $component  �Ӷ���
     * @return boolean  ɾ���Ƿ�ɹ�
     */
    public function remove(Component $component) 
    {
        foreach ($this->_composites as $key => $row) {
            if ($component == $row) {
                unset($this->_composites[$key]);
                return TRUE;
            }
        }
 
        return FALSE;
    }
 
    /**
     * �ۼ������� �������е��Ӷ���
     */
    public function getChild() 
    {
       return $this->_composites;
    }
 
}
 
class Leaf implements Component 
{
    private $_name;
 
    public function __construct($name) 
    {
        $this->_name = $name;
    }
 
    public function operation() 
    {
        echo 'Leaf operation ', $this->_name, '<br />';
    }
 
    public function getComposite() 
    {
        return null;
    }
 
    /**
     * �ۼ������� ���һ���Ӷ���,�˴�û�о���ʵ�֣�������һ��FALSE
     * @param Component $component  �Ӷ���
     */
    public function add(Component $component) 
    {
        return FALSE;
    }
 
    /**
     * �ۼ������� ɾ��һ���Ӷ���
     * @param Component $component  �Ӷ���
     * @return boolean  �˴�û�о���ʵ�֣�������һ��FALSE
     */
    public function remove(Component $component) 
    {
        return FALSE;
    }
 
    /**
     * �ۼ������� �������е��Ӷ��� �˴�û�о���ʵ�֣�����null
     */
    public function getChild() 
    {
       return null;
    } 
} 
 
/**
 * �ͻ���
 */
class Client 
{
     /**
     * Main program.
     */
    public static function main() 
    {
        $leaf1 = new Leaf('first');
        $leaf2 = new Leaf('second');
 
        $composite = new Composite();
        $composite->add($leaf1);
        $composite->add($leaf2);
        $composite->operation();
 
        $composite->remove($leaf2);
        $composite->operation(); 
    } 
}

Client::main();
?>
���Կ���͸��ʽ�ϳ�ģʽ��Leaf�и��ۼ���������ƽӹʵ��