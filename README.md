# Java-
Java实验项目仓库
# CPU
public class CPU {
	 int speed; 
	 String type;//属性
	 int getSpeed(){//构造一个方法返回速度
       return speed;
	 }
	 public void setSpeed(int speed){//把实参speed赋值给属性
	  this.speed=speed;//this.的应用
	 }
	 String gettype() {//构造一个方法返回type
		 return type;
	 }
	 public void settype(String type) {//同setspeed方法
		 this.type=type;
	 }
	}
  # PC
  public class PC {
	 CPU cpu;
	 HardDisk disk;
	 void setCPU(CPU cpu){
	  this.cpu=cpu;
	 }
	 void setHardDisk(HardDisk disk){
	  this.disk=disk; //原理同上
	 }
	 void show(){
	  System.out.println("CPU速度"+cpu.getSpeed());
	  System.out.println("CPU型号"+cpu.gettype());
	  System.out.println("硬盘容量"+disk.getAmount());
	  System.out.println("硬盘速度"+disk.getspeed2());//输出返回值并添加字符串解释
	 }
	 
}
# HardDisk
# Test
public class Test {
	public static void main(String args[]) {
	  //创建一个CPU对象
		CPU cpu =new CPU();
	  //将cpu的speed设置为2200
	    cpu.setSpeed(2200);
	  //cpu型号  
	    cpu.settype("i7-9750H");
	  //创建一个HardDisk对象
	    HardDisk disk=new HardDisk();
	  //将disk的amount设置为200
	    disk.setAmount(200);
	  //硬盘读写速度  
	    disk.setspeed2(500);
	  //创建一个PC对象
	    PC pc=new PC();
	    pc.setCPU(cpu);
	    pc.setHardDisk(disk);
	    pc.show();
	 }
}
设计思路：按照书上的思路写代码，并尽量添加使用构造方法以及方法的重构，Test函数则需要把各类对象以及方法联系到一起，调试了很久。
结果：CPU速度2200
     CPU型号i7-9750H
     硬盘容量200
     硬盘速度500
