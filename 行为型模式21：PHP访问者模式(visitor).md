PHP�е����ģʽ�ʼǣ�������ģʽ

��Visitorģʽ��
������ģʽ��ʾһ��������ĳ����ṹ�и�Ԫ�صĲ������������ڲ��޸ĸ�Ԫ�����ǰ���¶�����������ЩԪ�ص��²���������̬�����Ӿ�������߽�ɫ��
������ģʽ������˫�ط��ɡ��Ƚ������ߴ���Ԫ�ض����Accept�����У�Ȼ��Ԫ�ض����ٽ��Լ���������ߣ�֮�������ִ��Ԫ�ص���Ӧ������
������ģʽ�����ھۼ����Ͷ���������¡�����ͨ����ʽ�±����ж�ÿ��Ԫ��������ʲô����Ȼ�������Ӧ�Ĳ������Ӷ��������߳�������ת����䡣��������ģʽ����ԱȽϺõĽ��������⡣��ÿ��Ԫ��ͳһ����$element->accept($vistor)���ɡ�
������ģʽ�����ڱ����ʵ���ṹ�Ƚ��ȶ�������£����������������ࡣ������ģʽ�������ʽṹ����µķ�����
Visitorģʽʵ�����Ƿ����˶���ṹ�е�Ԫ�غͶ���ЩԪ�ؽ��в�������Ϊ���Ӷ�ʹ�����ڸ��ݶ���ṹ�е�Ԫ�ؽ��з������õ�ʱ�򣬲���Ҫʹ��IF����ж�
Ҳ���Ƿ�װ�˲���
���ǣ���������µ�Ԫ�ؽڵ㣬��ᵼ�°��������߽ӿڼ�������ĸı䣬��ͻ�Υ������������еĿ���ԭ��
�������������ʱ��һ���ʾ������ģʽ�Ѿ����ܲ��������ˣ�����˵���ʱ���������ˣ�
��Visitorģʽ�ṹͼ��

������ģʽ����ͼ

��Visitorģʽ����Ҫ��ɫ��
1)��������߽�ɫ(Visitor)��Ϊ�ö���ṹ(ObjectStructure)�е�ÿһ������Ԫ���ṩһ�����ʲ����ӿڡ��ò����ӿڵ����ֺͲ�����ʶ�� Ҫ���ʵľ���Ԫ�ؽ�ɫ�����������߾Ϳ���ͨ����Ԫ�ؽ�ɫ���ض��ӿ�ֱ�ӷ�������
2)��������߽�ɫ(ConcreteVisitor):ʵ�ֳ�������߽�ɫ�ӿ�����Ը�������Ԫ�ؽ�ɫ�����Ĳ�����
3)����ڵ㣨Node����ɫ:�ýӿڶ���һ��accept�������ܾ���ķ����ߡ�
4)����ڵ㣨Node����ɫ:ʵ�ֳ���ڵ��ɫ�е�accept������
5) ����ṹ��ɫ(ObjectStructure)������ʹ�÷�����ģʽ�ر��Ľ�ɫ����Ҫ�߱�������������ö������Ԫ�أ������ṩһ���߲�Ľӿ�������÷����߷�������Ԫ�أ�������һ�����ϣ����ģʽ������һ�����ϣ���һ���б��һ�����򼯺�(��PHP������ʹ��������棬��ΪPHP�е����鱾������һ�����Է����κ��������ݵļ���)

��Visitorģʽ����ȱ�㡿
������ģʽ�����µ��ŵ㣺
1)������ģʽʹ�������µĲ�����ú����ס�ʹ�÷�����ģʽ�����ڲ����޸ľ���Ԫ���������������µĲ���������Ҫ��ͨ��Ԫ�����accept����������һ���µ�visitor������ʵ�ֵġ����һЩ����������һ�����ӵĽṹ����Ļ�����ôһ����ԣ������µĲ�����ܸ��ӡ���ʹ�÷�����ģʽ�������µĲ�������ζ������һ���µķ������࣬��ˣ���ú����ס�
2)������ģʽ���йص���Ϊ���е�һ�������߶����У������Ƿ�ɢ��һ�����Ľڵ����С�
3)������ģʽ���Կ��������ĵȼ��ṹ�������ڲ�ͬ�ĵȼ��ṹ�ĳ�Ա�ࡣ������ֻ�ܷ�������ͬһ�����͵ȼ��ṹ�ĳ�Ա���󣬶����ܷ������ڲ�ͬ�ȼ��ṹ�Ķ��󡣷�����ģʽ����������һ�㡣
4)����״̬��ÿһ�������ķ����߶��󶼼�������ص���Ϊ���Ӷ�Ҳ�Ϳ����ڷ��ʵĹ����н�ִ�в�����״̬�������Լ��ڲ��������Ƿ�ɢ���ܶ�Ľڵ�����С�����������ϵͳά�����ŵ㡣

������ģʽ�����µ�ȱ�㣺
1)�����µĽڵ����ú����ѡ�ÿ����һ���µĽڵ㶼��ζ��Ҫ�ڳ�������߽�ɫ������һ���µĳ������������ÿһ���������������������Ӧ�ľ��������
2)�ƻ���װ��������ģʽҪ������߶�����ʲ�����ÿһ���ڵ����Ĳ�������������һ�������нڵ�����Ҫ�����Ǳ��뱩¶һЩ�Լ��Ĳ������ڲ�״̬����Ȼ�������ߵķ��ʾͱ��û�����塣���ڷ����߶����Լ�����۷��ʲ��������״̬���Ӷ�ʹ��Щ״̬���ٴ洢�ڽڵ�����У���Ҳ���ƻ���װ�ġ�

ʹ��Visitorģʽ��ǰ��: ����Ⱥ�ṹ��(Collection) �еĶ������ͺ��ٸı䡣
�ڽӿ�Visitor��Element��,ȷ��Element���ٱ仯,Ҳ����˵��ȷ������Ƶ��������µ�ElementԪ�����ͼӽ��������Ա仯���Ƿ�������Ϊ�������Ҳ����Visitor�Ĳ�ͬ��������ж���,����ʹ�÷�����ģʽ���.
������󼯺��еĶ��󼯺Ͼ����б仯, ��ô����Visitorʵ��Ҫ�仯��ConcreteVisitorҲҪ������Ӧ��Ϊ��GOF������,��������Щ��������ֱ������������������ʹ�÷��������ģʽ��

��Visitorģʽ������ģʽ��
1�����������Ľṹ���������Եģ�ʹ�õ���ģʽ�����Ƿ�����ģʽҲ�ǿ��Ե�
2��������ģʽ����ϳ�ģʽ��һЩ�ṹ����
�����������ԡ�Java��ģʽ��һ��

��VisitorģʽPHPʾ����
<?php
/**
 * ������ģʽ 2015-10-09
 * 1.Ŀ��
 * ������ģʽ��ʾһ��������ĳ����ṹ�и�Ԫ�صĲ������������ڲ��޸ĸ�Ԫ�����ǰ���¶�����������ЩԪ�ص��²���������̬�����Ӿ�������߽�ɫ
 * 2.ʹ�ó���
 * 2.1 ����Ⱥ�ṹ��(Collection) �еĶ������ͺ��ٸı䡣
 */

/**
 * ���������
 */
interface Visitor 
{
    public function visitConcreteElementA(ConcreteElementA $elementA);
    public function visitConcreteElementB(ConcreteElementB $elementB);
}

/**
 * ����Ԫ��
 */
interface Element
{
    public function accept(Visitor $visitor);
}
 
/**
 * ����ķ�����1
 */
class ConcreteVisitor1 implements Visitor
{
    public function visitConcreteElementA(ConcreteElementA $elementA) 
    {
        echo $elementA->getName() . " visitd by ConcerteVisitor1 <br />";
    }
 
    public function visitConcreteElementB(ConcreteElementB $elementB) 
    {
        echo $elementB->getName() . " visited by ConcerteVisitor1 <br />";
    }
}
 
/**
 * ����ķ�����2
 */
class ConcreteVisitor2 implements Visitor
{
    public function visitConcreteElementA(ConcreteElementA $elementA) 
    {
        echo $elementA->getName() . " visitd by ConcerteVisitor2 <br />";
    }
 
    public function visitConcreteElementB(ConcreteElementB $elementB) 
    {
        echo $elementB->getName() . " visited by ConcerteVisitor2 <br />";
    }
}
 
/**
 * ����Ԫ��A
 */
class ConcreteElementA implements Element 
{
    private $_name;
 
    public function __construct($name) 
    {
        $this->_name = $name;
    }
 
    public function getName() 
    {
        return $this->_name;
    }
 
    /**
     * ���ܷ����ߵ�������Ը�Ԫ�ص��·���
     * @param Visitor $visitor
     */
    public function accept(Visitor $visitor) 
    {
        $visitor->visitConcreteElementA($this);
    }
}
 
/**
 *  ����Ԫ��B
 */
class ConcreteElementB implements Element
{
    private $_name;
 
    public function __construct($name) 
    {
        $this->_name = $name;
    }
 
    public function getName() 
    {
        return $this->_name;
    }
 
    /**
     * ���ܷ����ߵ�������Ը�Ԫ�ص��·���
     * @param Visitor $visitor
     */
    public function accept(Visitor $visitor) 
    {
        $visitor->visitConcreteElementB($this);
    }
}
 
/**
 * ����ṹ ��Ԫ�صļ���
 */
class ObjectStructure
{
    private $_collection;
 
    public function __construct() 
    {
        $this->_collection = array();
    }
 
 
    public function attach(Element $element) 
    {
        return array_push($this->_collection, $element);
    }
 
    public function detach(Element $element) 
    {
        $index = array_search($element, $this->_collection);
        if ($index !== FALSE) {
            unset($this->_collection[$index]);
        }
 
        return $index;
    }
 
    public function accept(Visitor $visitor) 
    {
        foreach ($this->_collection as $element) {
            $element->accept($visitor);
        }
    }
}
 
class Client
{ 
    /**
     * Main program.
     */
    public static function main() 
    {
        $elementA = new ConcreteElementA("ElementA");
        $elementB = new ConcreteElementB("ElementB");
        $elementA2 = new ConcreteElementB("ElementA2");
        $visitor1 = new ConcreteVisitor1();
        $visitor2 = new ConcreteVisitor2();
 
        $os = new ObjectStructure();
        $os->attach($elementA);
        $os->attach($elementB);
        $os->attach($elementA2);
        $os->detach($elementA);
        $os->accept($visitor1);
        $os->accept($visitor2);
    }
}
 
Client::main();
?>