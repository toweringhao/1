PHP���ģʽ�ʼǣ�ʹ��PHPʵ�ֳ��󹤳�ģʽ
���󹤳�ģʽ��Abstact Factory����һ�ֳ�����������ģʽ����ģʽΪһ����Ʒ���ṩ��ͳһ�Ĵ����ӿڡ�����Ҫ�����Ʒ���ĳһϵ�е�ʱ�򣬿���Ϊ��ϵ�еĲ�Ʒ�崴��һ������Ĺ����ࡣ

����ͼ��
���󹤳�ģʽ�ṩһ������һϵͳ��ػ��໥��������Ľӿڣ�������ָ�����Ǿ�����ࡾGOF95��

�����󹤳�ģʽ�ṹͼ��

���󹤳�ģʽ

�����󹤳�ģʽ����Ҫ��ɫ��
���󹤳�(Abstract Factory)��ɫ��������һ�����������Ʒ����Ľӿڡ�ͨ���Խӿڻ������ʵ�֣����еľ��幤�������ʵ������ӿڻ�̳�����ࡣ
���幤��(Concrete Factory)��ɫ��ʵ�ִ�����Ʒ����Ĳ������ͻ���ֱ�ӵ��������ɫ������Ʒ��ʵ���������ɫ������ѡ����ʵĲ�Ʒ������߼���ͨ��ʹ�þ�����ʵ�֡�
�����Ʒ(Abstract Product)��ɫ������һ���Ʒ�Ľӿڡ����ǹ�������ģʽ�������Ķ���ĸ��࣬�����ǹ�ͬӵ�еĽӿڡ�
�����Ʒ(Concrete Product)��ɫ��ʵ�ֳ����Ʒ��ɫ������Ľӿڣ�����һ��������Ӧ�ľ��幤�������Ĳ�Ʒ�������ڲ�������Ӧ�ó����ҵ���߼���

�����󹤳�ģʽ����ȱ�㡿
���󹤳�ģʽ���ŵ�:
1�������˾������
2��ʹ���ӻ��滻��Ʒ��������
3�������ڲ�Ʒ��һ����
���󹤳�ģʽ��ȱ��: ����֧��������Ĳ�Ʒ��������ΪAbstractFactory�ӿ�ȷ���˿��Ա������Ĳ�Ʒ���ϡ�֧���¸���Ĳ�Ʒ����Ҫ��չ�ù����ӿڣ��Ӷ�����AbstractFactory�༰����������ĸı䡣
���󹤳�������һ����б�ķ�ʽ֧�������µĲ�Ʒ�У���Ϊ�²�Ʒ��������ṩ�˷��㣬������Ϊ�µĲ�Ʒ�ȼ��ṹ�������ṩ�����ķ��㡣

�����󹤳�ģʽ���ó�����
�������Ӧ��ʹ�ó��󹤳�ģʽ��
1��һ��ϵͳ��Ӧ�������ڲ�Ʒ��ʵ����α���������Ϻͱ���ϸ�ڣ������������̬�Ĺ���ģʽ������Ҫ�ġ�
2�����ϵͳ�Ĳ�Ʒ�ж���һ���Ĳ�Ʒ�壬��ϵͳֻ��������ĳһ��Ĳ�Ʒ��
3�� ͬ����ͬһ����Ʒ��Ĳ�Ʒ����һ��ʹ�õģ���һԼ��������ϵͳ����������ֳ�����
4��ϵͳ�ṩһ����Ʒ��Ŀ⣬���еĲ�Ʒ��ͬ���Ľӿڳ��֣��Ӷ�ʹ�ÿͻ��˲�������ʵ��

��Java��ģʽ189ҳ��

Abstract Factoryģʽ�ļ���Ҫ�㣺
1�����û��Ӧ�ԡ���ϵ�ж��󹹽���������仯����û�б�Ҫʹ��Abstract Factoryģʽ��
2����ϵ�ж���ָ�����������֮�����໥�����������õĹ�ϵ��
3��Abstract Factoryģʽ��Ҫ����Ӧ�ԡ���ϵ�С�������䶯��ȱ��������Ӧ��
���¶��󡱵�����䶯����һ��Ӧ��ע�⣬����ǰ��˵�ģ������������Ҫ�ڼ���
����ϵ�е��࣬����ĸĶ���ܴ�
4��Abstract Factoryģʽ������Factory Methodģʽ��ͬ�����Ӧ��
�����󴴽���������仯��

���󹤳��е�����
1. �ڲ�Ʒ�ȼ��ṹ����Ŀ���������£������µĲ�Ʒ�壬����ζ����ÿһ����Ʒ�ȼ��ṹ������һ�������߶�����µľ��� �����߳���;��壩��Ʒ��ɫ�� ���ڹ����ȼ��ṹ�����Ʒ�ȼ��ṹƽ�еĵǼǻ�������ˣ�����Ʒ�ȼ��ṹ��������ʱ�� ��Ҫ�������ȼ��ṹ����Ӧ�ĵ��������ڲ�Ʒ�ȼ��ṹ�г������µ�Ԫ�أ���ˣ� ��Ҫ�򹤳��ȼ��ṹ�м�����Ӧ����Ԫ�ؾͿ����ˡ� ����֮�����ʦֻ��Ҫ��ϵͳ�м����µľ��幤����Ϳ����ˣ�û�б�Ҫ�޸��� �еĹ�����ɫ���߲�Ʒ��ɫ����ˣ���ϵͳ�еĲ�Ʒ������ʱ�����󹤳�ģʽ��֧�֡���-�ա�ԭ��ġ�

2. �ڲ�Ʒ�����Ŀ���������£������µĲ�Ʒ�ȼ��ṹ������֮�����еĲ�Ʒ�ȼ��ṹ �еĲ�Ʒ��Ŀ����ı䣬�������ڶ��һ�������еĲ�Ʒ�ȼ��ṹƽ�е��µĲ�Ʒ�ȼ��ṹ�� Ҫ������һ�㣬����Ҫ�޸����еĹ�����ɫ����ÿһ�������඼����һ���µĹ��������� ������Ȼ��Υ�������C�ա�ԭ��ġ�����֮�����ڲ�Ʒ�ȼ��ṹ�����ӣ����󹤳�ģʽ�ǲ�֧�֡����C�ա�ԭ��ġ�

�ۺ����������ǿ���֪���������еĳ����Ʒ�����������Ʒ��֧�֡�������ԭ�򡱣� Ȼ�������������Ʒʱ��ȷ��֧�֡������ա�ԭ�򡣳��󹤳�ģʽ��һ����б�� ��ʽ֧�������µĲ�Ʒ����Ϊ�²�Ʒ��������ṩ���㣬������Ϊ�µĲ�Ʒ�ȼ� �ṹ�������ṩ�����ķ��㡣

�����󹤳�ģʽ������ģʽ��
����ģʽ(singletonģʽ)�����幤���������Ƴɵ�����,���ڹ���ͨ����һ���Ϳ��ԣ���˾��幤������һ�㶼ʵ��Ϊһ��Singleton��
��������ģʽ(factory methodģʽ)�����󹤳�������Ʒ�ķ�������Ϊ����������
ԭ��ģʽ(prototypeģʽ)������ж�����ܵĲ�Ʒϵ�У�����Ĺ���Ҳ����ʹ��ԭ��ģʽ�����幤��ʹ�ò�Ʒϵ����
ÿһ����Ʒ��ԭ�ͽ���ʵ��������ͨ����������ԭ���������µĲ�Ʒ��

�����󹤳�ģʽPHPʾ����
<?php
/**
 * ���󹤳�ģʽ 2015-10-09
 * 1.Ŀ��
 * ���󹤳�ģʽ�ṩһ������һϵͳ��ػ��໥��������Ľӿڣ�������ָ�����Ǿ������
 * 2.ʹ�ó���
 * 2.1 һ��ϵͳ��Ӧ�������ڲ�Ʒ��ʵ����α���������Ϻͱ���ϸ�ڣ������������̬�Ĺ���ģʽ������Ҫ��
 * 2.2 ���ϵͳ�Ĳ�Ʒ�ж���һ���Ĳ�Ʒ�壬��ϵͳֻ��������ĳһ��Ĳ�Ʒ
 * 2.3 ͬ����ͬһ����Ʒ��Ĳ�Ʒ����һ��ʹ�õģ���һԼ��������ϵͳ����������ֳ���
 * 2.4 ϵͳ�ṩһ����Ʒ��Ŀ⣬���еĲ�Ʒ��ͬ���Ľӿڳ��֣��Ӷ�ʹ�ÿͻ��˲�������ʵ��
 */
 
/**
 * ���󹤳�
 */
interface AbstractFactory 
{
    /**
     * �����ȼ��ṹΪA�Ĳ�Ʒ�Ĺ�������
     */
    public function createProductA();
 
     /**
     * �����ȼ��ṹΪB�Ĳ�Ʒ�Ĺ�������
     */
    public function createProductB();
}
 
/**
 * ���幤��1
 */
class ConcreteFactory1 implements AbstractFactory
{
 
    public function createProductA() 
    {
        return new ProductA1();
    }
 
    public function createProductB() 
    {
        return new ProductB1();
    }
} 
 
/**
 * ���幤��2
 */
class ConcreteFactory2 implements AbstractFactory
{ 
    public function createProductA() 
    {
        return new ProductA2();
    }
 
    public function createProductB() 
    {
        return new ProductB2();
    }
}
 
/**
 * �����ƷA
 */
interface AbstractProductA 
{ 
    /**
     * ȡ�ò�Ʒ��
     */
    public function getName();
}
 
/**
 * �����ƷB
 */
interface AbstractProductB 
{ 
    /**
     * ȡ�ò�Ʒ��
     */
    public function getName();
}
 
/**
 * �����Ʒ��1
 */
class ProductA1 implements AbstractProductA 
{
    private $_name;
 
    public function __construct() 
    {
        $this->_name = 'product A1';
    }
 
    public function getName() 
    {
        return $this->_name;
    }
}
 
/**
 * �����Ʒ��2
 */
class ProductA2 implements AbstractProductA 
{
    private $_name;
 
    public function __construct() 
    {
        $this->_name = 'product A2';
    }
 
    public function getName() 
    {
        return $this->_name;
    }
}
 
/**
 * �����ƷB1
 */
class ProductB1 implements AbstractProductB 
{
    private $_name;
 
    public function __construct() 
    {
        $this->_name = 'product B1';
    }
 
    public function getName() 
    {
        return $this->_name;
    }
}
 
/**
 * �����ƷB2
 */
class ProductB2 implements AbstractProductB 
{
    private $_name;
 
    public function __construct() 
    {
        $this->_name = 'product B2';
    }
 
    public function getName() 
    {
        return $this->_name;
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
        self::run(new ConcreteFactory1());
        self::run(new ConcreteFactory2());
    }
 
    /**
     * ���ù���ʵ�����ɲ�Ʒ�������Ʒ��
     * @param   $factory    AbstractFactory     ����ʵ��
     */
    public static function run(AbstractFactory $factory) 
    {
        $productA = $factory->createProductA();
        $productB = $factory->createProductB();
        echo $productA->getName(), '<br />';
        echo $productB->getName(), '<br />';
    } 
}
 
Client::main();
?>