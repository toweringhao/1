PHP���ģʽ�ʼǣ�ʹ��PHPʵ��������ģʽ

����ͼ��
��һ����Ľӿ�ת���ɿͻ�ϣ��������һ���ӿڡ�Adapterģʽʹ��ԭ�����ڽӿڲ����ݶ�����һ�������Ǵ������һ����
��GOF95��

��������ģʽ�ṹͼ��

��������


����������


��������ģʽ����Ҫ��ɫ��
Ŀ��(Target)��ɫ������ͻ���ʹ�õ����ض�������صĽӿڣ���Ҳ�����������ڴ��õ���
Դ(Adaptee)��ɫ����Ҫ��������Ľӿ�
������(Adapter)��ɫ����Adaptee�Ľӿ���Target�ӿڽ������䣻�������Ǳ�ģʽ�ĺ��ģ���������Դ�ӿ�ת����Ŀ��ӿڣ��˽�ɫΪ������

��������ģʽ���ó�����
1������ʹ��һ���Ѿ����ڵ��࣬�����Ľӿڲ������������
2�����봴��һ�����Ը��õ��࣬�����������������ص���򲻿�Ԥ������Эͬ����
3������ʹ��һ���Ѿ����ڵ����࣬���ǲ����ܶ�ÿһ�����������໯��ƥ�����ǵĽӿڡ����������������������ĸ���ӿڣ������ڶ�����������

����������ģʽ�������������
����������Adapter��Adaptee�Ǽ̳й�ϵ
1����һ�������Adapter���Target����ƥ�䡣����ǵ�������Ҫһ��ƥ��һ�����Լ�������������ʱ����Adapter������ʤ�ι���
2��ʹ��Adapter�����ض���Adaptee�Ĳ�����Ϊ����ΪAdapter��Adaptee��һ���Ӽ�
3����������һ�����󣬲�����Ҫ�����ָ���Լ��ȡ��adaptee

������������Adapter��Adaptee��ί�й�ϵ
1������һ��Adapter����Adapteeͬʱ������AdapterҲ����һ�θ����е�Adaptee��ӹ���
2��ʹ���ض���Adaptee����Ϊ�Ƚ�����

��������ģʽ������ģʽ��
����ģʽ(bridgeģʽ)������ģʽ��������������ƣ���������ģʽ�ĳ����㲻ͬ������ģʽĿ���ǽ��ӿڲ��ֺ�ʵ�ֲ��ַ��룬�Ӷ������ǿ��Խ�Ϊ����Ҳ��Զ����ļ��Ըı䡣������������ģʽ����ζ�Ÿı�һ�����ж���Ľӿ�
װ����ģʽ(decoratorģʽ)��װ��ģʽ��ǿ����������Ĺ��ܶ�ͬʱ�ֲ��ı����Ľӿڡ����װ��ģʽ��Ӧ�õ�͸���Ա����������á�

����������ģʽPHPʾ����
��������ʹ�õ��Ǽ̳�
 <?php
/**
 * ��������ģʽ 2015-10-09
 * 1.Ŀ��
 * ��һ����Ľӿ�ת���ɿͻ�ϣ��������һ���ӿڡ�Adapterģʽʹ��ԭ�����ڽӿڲ����ݶ�����һ�������Ǵ������һ����
 * 2.ʹ�ó���
 * 2.1 ����ʹ��һ���Ѿ����ڵ��࣬�����Ľӿڲ������������
 * 2.2 ���봴��һ�����Ը��õ��࣬�����������������ص���򲻿�Ԥ������Эͬ����
 * 2.3 ����ʹ��һ���Ѿ����ڵ����࣬���ǲ����ܶ�ÿһ�����������໯��ƥ�����ǵĽӿڡ����������������������ĸ���ӿڣ������ڶ�����������
 */

/**
 * Ŀ���ɫ
 */
interface Target 
{ 
    /**
     * Դ��Ҳ�еķ���1
     */
    public function sampleMethod1();
 
    /**
     * Դ��û�еķ���2
     */
    public function sampleMethod2();
}
 
/**
 * Դ��ɫ
 */
class Adaptee 
{ 
    /**
     * Դ�ຬ�еķ���
     */
    public function sampleMethod1() 
    {
        echo 'Adaptee sampleMethod1 <br />';
    }
}
 
/**
 * ����������ɫ
 */
class Adapter extends Adaptee implements Target 
{ 
    /**
     * Դ����û��sampleMethod2�������ڴ˲���
     */
    public function sampleMethod2() 
    {
        echo 'Adapter sampleMethod2 <br />';
    } 
}
 
class Client 
{ 
    /**
     * Main program.
     */
    public static function main() 
    {
        $adapter = new Adapter();
        $adapter->sampleMethod1();
        $adapter->sampleMethod2(); 
    } 
}
 
Client::main();
?>

������������ģʽPHPʾ����
����������ʹ�õ���ί��

<?php
/**
 * ����������ģʽ
 */
 
/**
 * Ŀ���ɫ
 */
interface Target 
{ 
    /**
     * Դ��Ҳ�еķ���1
     */
    public function sampleMethod1();
 
    /**
     * Դ��û�еķ���2
     */
    public function sampleMethod2();
}
 
/**
 * Դ��ɫ
 */
class Adaptee 
{ 
    /**
     * Դ�ຬ�еķ���
     */
    public function sampleMethod1() 
    {
        echo 'Adaptee sampleMethod1 <br />';
    }
}
 
/**
 * ����������ɫ
 */
class Adapter implements Target 
{ 
    private $_adaptee;
 
    public function __construct(Adaptee $adaptee) 
    {
        $this->_adaptee = $adaptee;
    }
 
    /**
     * ί�ɵ���Adaptee��sampleMethod1����
     */
    public function sampleMethod1() 
    {
        $this->_adaptee->sampleMethod1();
    }
 
    /**
     * Դ����û��sampleMethod2�������ڴ˲���
     */
    public function sampleMethod2() 
    {
        echo 'Adapter sampleMethod2 <br />';
    } 
}
 
class Client 
{ 
    /**
     * Main program.
     */
    public static function main() 
    {
        $adaptee = new Adaptee();
        $adapter = new Adapter($adaptee);
        $adapter->sampleMethod1();
        $adapter->sampleMethod2(); 
    } 
}
 
Client::main();
?>
