PHP���ģʽ�ʼǣ�ʹ��PHPʵ�ֹ���ģʽ

����ͼ��
����һ�����ڴ�������Ľӿڣ����������ʵ������һ���ࡣFactory Methodʹ��һ�����ʵ�����ӳٵ������ࡾGOF95��

������ģʽ�ṹͼ��

��������ģʽ

������ģʽ����Ҫ��ɫ��
�����Ʒ(Product)��ɫ�������Ʒ�����еĸ����ӿ�
�����Ʒ(Concrete Product)��ɫ��ʵ�ֳ����Ʒ��ɫ������Ľӿڣ����ҹ�������ģʽ��������ÿһ��������ĳ�����Ʒ�����ʵ��
���󹤳�(Creator)��ɫ��ģʽ���κδ�������Ĺ����඼Ҫʵ������ӿڣ��������˹����������÷�������һ��Product���͵Ķ���
CreatorҲ���Զ���һ������������ȱʡʵ�֣�������һ��ȱʡ�ĵ�ConcreteProduct����
���幤��(Concrete Creator)��ɫ��ʵ�ֳ��󹤳��ӿڣ����幤����ɫ��Ӧ���߼���أ���Ӧ�ó���ֱ�ӵ����Դ�����Ʒ����

������ģʽ���ŵ��ȱ�㡿
����ģʽ���ŵ�
��������ģʽ��������ϵͳ�ڲ��޸Ĺ�����ɫ������������²�Ʒ��

����ģʽ��ȱ��
�ͻ����ܽ���Ϊ�˴���һ���ض���ConcreteProduct���󣬾Ͳ��ò�����һ��Creator����

������ģʽ���ó�����
1����һ���಻֪���������봴���Ķ�������ʱ��
2����һ����ϣ��������������ָ�����������Ķ����ʱ��
3�����ཫ���������ְ��ί�и�������������ĳһ����������ϣ������һ�����������Ǵ�������һ��Ϣ�ֲ�����ʱ��

������ģʽ������ģʽ��
���󹤳�ģʽ(abstract factoryģʽ)��Abstract Factoryģʽ����ʹ�ù���������ʵ��
Template Methodģʽ: ��������ͨ����Template Methods�б�����

������ģʽPHPʾ����
 <?php
/**
 * ����ģʽ 2015-10-09
 * 1.Ŀ��
 * ����һ�����ڴ�������Ľӿڣ����������ʵ������һ���ࡣFactory Methodʹ��һ�����ʵ�����ӳٵ�������
 * 2.ʹ�ó���
 * 2.1 ��һ���಻֪���������봴���Ķ�������ʱ��
 * 2.2 ��һ����ϣ��������������ָ�����������Ķ����ʱ��
 * 2.3 ���ཫ���������ְ��ί�и�������������ĳһ����������ϣ������һ�����������Ǵ�������һ��Ϣ�ֲ�����ʱ��
 */

/**
 * ���󹤳���ɫ
 */
interface Creator 
{
    public function factoryMethod();
}
 
/**
 * ���幤����ɫA
 */
class ConcreteCreatorA implements Creator 
{ 
    /**
     * �������� ���ؾ��� ��ƷA
     * @return ConcreteProductA
     */
    public function factoryMethod() 
    {
        return new ConcreteProductA();
    }
}
 
/**
 * ���幤����ɫB
 */
class ConcreteCreatorB implements Creator 
{ 
    /**
     * �������� ���ؾ��� ��ƷB
     * @return ConcreteProductB
     */
    public function factoryMethod() 
    {
        return new ConcreteProductB();
    }
}
 
/**
 * �����Ʒ��ɫ
 */
interface Product 
{
    public function operation();                                                                                    
}
 
/**
 * �����Ʒ��ɫA
 */
class ConcreteProductA implements Product 
{ 
    /**
     * �ӿڷ���ʵ�� ����ض��ַ���
     */
    public function operation() 
    {
        echo 'ConcreteProductA <br />';
    }
}
 
/**
 * �����Ʒ��ɫB
 */
class ConcreteProductB implements Product 
{ 
    /**
     * �ӿڷ���ʵ�� ����ض��ַ���
     */
    public function operation() 
    {
        echo 'ConcreteProductB <br />';
    }
}
 
class Client 
{
    /**
     * Main program.
     */
    public static function main() 
    {
        $creatorA = new ConcreteCreatorA();
        $productA = $creatorA->factoryMethod();
        $productA->operation();
 
        $creatorB = new ConcreteCreatorB();
        $productB = $creatorB->factoryMethod();
        $productB->operation();
    }                                                
}
 
Client::main();
?>

����������ģʽ��򵥹���ģʽ��
��������ģʽ��򵥹���ģʽ�ٽṹ�ϵĲ�ͬ���Ǻ����ԡ�����������ĺ�����һ�����󹤳��࣬���򵥹���ģʽ�Ѻ��ķ���һ���������ϡ�
��������ģʽ֮������һ�������ж�̬�Թ���ģʽ����Ϊ���幤���඼�й�ͬ�Ľӿڣ������й�ͬ�ĳ����ࡣ
��ϵͳ��չ��Ҫ����µĲ�Ʒ����ʱ��������Ҫ���һ����������Լ�һ�����幤������ԭ�й���������Ҫ�����κ��޸ģ�Ҳ����Ҫ�޸Ŀͻ��ˣ��ܺõķ����ˡ����ţ���ա�ԭ�򡣶��򵥹���ģʽ������²�Ʒ����󲻵ò��޸Ĺ�����������չ�Բ��á�
��������ģʽ�˻�������ݱ�ɼ򵥹���ģʽ��