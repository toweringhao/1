PHP���ģʽ�ʼǣ�ʹ��PHPʵ��װ��ģʽ

����ͼ��
��̬�ĸ�һ���������һЩ�����ְ�𡣾����ӹ�����˵��Decoratorģʽ������������Ϊ��GOF95��
װ��ģʽ���ԶԿͻ�͸���ķ�ʽ��̬�ظ�һ�����󸽼��ϸ����ְ����Ҳ����˵���ͻ��˲�������ö�����װ��ǰ��װ�κ���ʲô��ͬ��װ��ģʽ�����ڲ�ʹ�ô���������������£�������Ĺ��ܼ�����չ��

��װ��ģʽ�ṹͼ��

װ��ģʽ

��װ��ģʽ����Ҫ��ɫ��
���󹹼�(Component)��ɫ������һ������ӿڣ��Թ淶׼�����ո���ְ��Ķ��󣬴Ӷ����Ը���Щ����̬�����ְ��
���幹��(Concrete Component)��ɫ������һ����Ҫ���ո���ְ����ࡣ
װ��(Decorator)��ɫ������һ��ָ��Component�����ָ�룬������һ����Component�ӿ�һ�µĽӿڡ�
����װ��(Concrete Decorator)��ɫ������������������Ӹ��ӵ�ְ��

��װ��ģʽ����ȱ�㡿
װ��ģʽ���ŵ�:
1���Ⱦ�̬�̳и���
2�������ڲ�νṹ�߲������̫�������
װ��ģʽ��ȱ�㣺
1��ʹ��װ��ģʽ�������ʹ�ü̳й�ϵ����Ķ��󡣲�����Щ������ȥ�������񣬴Ӷ�ʹ�ò�������ѡ�

��װ��ģʽ���ó�����
1���ڲ�Ӱ���������������£��Զ�̬��͸���ķ�ʽ�������������ְ��
2��������Щ���Գ�����ְ�𣬼���Ҫ��̬�ĸ�һ��������ӹ��ܲ�����Щ�����ǿ��Զ�̬�ĳ����ġ�
3�������ܲ���������ķ�����������ʱ��һ������ǣ������д�����������չ��Ϊ֧��ÿһ����Ͻ��������������࣬ʹ��������Ŀ�ʱ�ը����������һ�������������Ϊ�ඨ�屻���أ����ඨ�岻�������������ࡣ

��װ��ģʽ������ģʽ��

��װ��ģʽPHPʾ����
<?php
/**
 * װ��ģʽ 2015-10-09
 * 1.Ŀ��
 * ��̬�ĸ�һ���������һЩ�����ְ�𡣾����ӹ�����˵��Decoratorģʽ������������Ϊ���
 * 2.ʹ�ó���
 * 2.1 �ڲ�Ӱ���������������£��Զ�̬��͸���ķ�ʽ�������������ְ��
 * 2.2 ������Щ���Գ�����ְ�𣬼���Ҫ��̬�ĸ�һ��������ӹ��ܲ�����Щ�����ǿ��Զ�̬�ĳ����ġ�
 * 2.3 �����ܲ���������ķ�����������ʱ��һ������ǣ������д�����������չ��Ϊ֧��ÿһ����Ͻ��������������࣬ʹ��������Ŀ�ʱ�ը����������һ�������������Ϊ�ඨ�屻���أ����ඨ�岻�������������ࡣ
 */

/**
 * ���󹹼���ɫ
 */
interface Component 
{
    /**
     * ʾ������
     */
    public function operation();
}
 
/**
 * װ�ν�ɫ
 */
abstract class Decorator implements Component
{ 
    protected  $_component;
 
    public function __construct(Component $component) 
    {
        $this->_component = $component;
    }
 
    public function operation() 
    {
        $this->_component->operation();
    }
}
 
/**
 * ����װ����A
 */
class ConcreteDecoratorA extends Decorator 
{
    public function __construct(Component $component) 
    {
        parent::__construct($component);
 
    }
 
    public function operation() 
    {
        parent::operation();    //  ����װ����Ĳ���
        $this->addedOperationA();   //  �����ӵĲ���
    }
 
    /**
     * �����ӵĲ���A����װ���ϵĹ���
     */
    public function addedOperationA() 
    {
        echo 'Add Operation A <br />';
    }
}
 
/**
 * ����װ����B
 */
class ConcreteDecoratorB extends Decorator 
{
    public function __construct(Component $component) 
    {
        parent::__construct($component); 
    }
 
    public function operation() 
    {
        parent::operation();
        $this->addedOperationB();
    }
 
    /**
     * �����ӵĲ���B����װ���ϵĹ���
     */
    public function addedOperationB() 
    {
        echo 'Add Operation B <br />';
    }
}
 
/**
 * ���幹��
 */
class ConcreteComponent implements Component
{ 
    public function operation() 
    {
        echo 'Concrete Component operation <br />';
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
        $component = new ConcreteComponent();
        $decoratorA = new ConcreteDecoratorA($component);
        $decoratorB = new ConcreteDecoratorB($decoratorA);
        $decoratorC = new ConcreteDecoratorB($component);
 
        $decoratorA->operation();
        $decoratorB->operation();
    } 
}
 
Client::main();
?>
������ʾ�����Կ�����
1��װ��������һ������$_component��������������Component;
2��װ����ʵ����Component�ӿ�;
3���ӿڵ�ʵ����ί�ɸ����࣬�������ǵ�����ί�ɣ����й��ܵ���ǿ;
4������װ����ʵ���˳���װ�����operation������