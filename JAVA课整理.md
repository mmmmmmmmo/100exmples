```java
package jin;

import java.util.HashSet;
import java.util.Iterator;

public class day2 {
	public static void main(String[] args){
		m2();
	}
private static void m1(){
	HashSet set=new HashSet();
	//
	set.add("zhangsan");
	set.add("lisi");
	set.add("wangwu");
	System.out.println(set);
	boolean b=set.contains("lisi");
	System.out.println(b);

}
private static void m2(){
	HashSet set=new HashSet();
	//
	set.add("zhangsan");
	set.add("lisi");
	set.add("wangwu");
	Iterator ite=set.iterator();
	while(ite.hasNext()){
		System.out.println(ite.next());
	}
}
//判断一个元素是否存在集合中
	
}
package jin;
import java.util.Iterator;
import java.util.ArrayList;
import java.util.LinkedList;
//集合java
//collection 集合
//list 有序重复
//ArrayList 
//2.set 接口 无序，不可重复
//HashSet
//Map接口 键值对的形式
//Hashmap
public class 集合 {
	public static void main (String[] args){
	m1();}
		private static void m1(){
		LinkedList  list=new LinkedList();
		list.push("a");
		list.push("b");
		list.push("c");
		list.push("a");
		System.out.println(list.size());
		System.out.println(list);
		//for(int i=0;i<list.size();i++){
			//String v
		//迭代器遍历集合元素
		
		/*Iterator ite=list.iterator();
		while(ite.hasNext()){
			System.out.println(ite.next());*/
		
	}
	
	private static void m3(){
		ArrayList list=new ArrayList();
		list.add("a");
		list.add("b");
		list.add("c");
		list.add("123");
		System.out.println(list);
		//根据索引删除
		list.remove("b");
		System.out.println(list);
		/*
		 * 修改指定位置的元素
		 */
		list.set(2,"r");
		System.out.println(list);
		String v=(String)list.get(0);
		System.out.println(list);
	}
	
	
	/*
	 * ArrayList 添加删除操作

	 * */
	
}

package jin;

import java.security.KeyStore.Entry;
import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;

public class hashmap {
	public static void main(String[] args){
		m2();
	}
	/*
	 * 操作
	 */
	private static void m1(){
		HashMap map=new HashMap();
		map.put("a", "苹果");
		map.put("b", "葡萄");
		map.put("c", "西瓜");
		String v=(String)map.get("b");
		System.out.println(v);
		//删除
		map.remove("a");
		System.out.println(map);
	}
	public static void m2(){
		HashMap map=new HashMap();
		map.put("a", "苹果");
		map.put("b", "葡萄");
		map.put("c", "西瓜");
		
		Set set=map.entrySet();
		Iterator ite=set.iterator();
		while(ite.hasNext()){
			/*Map.Entry entry=(Entry)ite.next();
			System.out.println(entry.getKey()+"="+entry.);*/
			Map.Entry entry=(Map.Entry)ite.next();
			String key=(String)entry.getKey();
			if("b".equals(key)){
				entry.setValue("红葡萄");
			}
		}
		System.out.println(map);
	}
	
}
package newworld;

public class Fault3 extends Exception{
	// TODO Auto-generated method stub
//	try {
//		m1();
//	}catch(ArrayIndexOutOfBoundsException e){
//		e.printStackTrace();
//	}catch(NullPointerException e){
//		e.printStackTrace();
//	}
//	
//}
//public static void m1()
//{
////	{
////		if(throw new ArrayIndexOutOfBoundsException)
////	}
//	m2();
//	
//}
//private static void m2() {
//	// TODO Auto-generated method stub
//	int[2] a=new int[];
//	a[2]=2;
//}
}
package newworld;

import java.io.File;
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.LineNumberInputStream;

import javax.tools.FileObject;

public class llll {

	public static void main(String[] args)throws IOException{
		
//		File file1 = new File("d:\\File01.txt");
//		if (!file1.exists())
//		{
//			file1.createNewFile();
//		}
//		FileOutputStream fos = new FileOutputStream(file1);
//		String content = "Andriod";
//		byte[] bytes = content.getBytes();
//		fos.write(bytes);
		copyText();
		
	}

	
	public static void readText() throws IOException{
		File file=new File("D:\\File01.txt");
		FileInputStream fis=new FileInputStream(file);
		byte [] bytes=new byte[(int)file.length()];
		fis.read(bytes);
		System.out.println(new String(bytes));
		fis.close();
	}
	public static void copyText() throws IOException{
		//指定原文件和目标文件的路径
				File fileSrc = new File("D://files") ;
				File fileDes = new File("D://dir/fileNew") ;
				//读写源文件到内存
				byte[] bytes =  new byte[(int)fileSrc.length()] ;
				FileInputStream fis = new FileInputStream(fileSrc);
				fis.read(bytes) ;
				fis.close();
				//将读取到的内容写入制定的目标文件
				//判断父目录是否存在
				FileInputStream fis = new FileInputStream(fileSrc);
				byte[] bytes=new byte[3];
				while(fis.read(bytes)!=-1){
					
				}
				File dir =  new File( "D:/Codeblocks/dir");
				if( !dir.exists() )
				{
					System.out.println("父目录不存在,创建此目录");
					dir.mkdirs();
				}
				FileOutputStream fos = new FileOutputStream(fileDes);
				fos.write(bytes);
				fos.close();
			}

		
	}
	
package newworld;
 
public class lunchur {

	public static void main(String[] args) {
		
	try{caculate(1,2);
	
	}catch(Fault e){
		e.printStackTrace();
	}catch(Fault2 e){
		e.printStackTrace();
	}catch(Fault3 e){
		e.printStackTrace();
	}
	}
	public static void caculate(int a,int b){
		if(true){
			throw new Fault();
		}
		if(true){
			throw new Fault2();
		}
		if(true){
			throw new Fault3();
		}
	}





