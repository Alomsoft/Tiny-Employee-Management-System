import java.util.InputMismatchException;
import java.util.Scanner;
import java.io.*;
public class EmployeeRunner{
	public static void main(String[] args){
		
		try{
		Scanner sc = new Scanner(System.in);
		Address address = new Address();
		System.out.print("Enter House No: ");
		address.setHouseNo(sc.nextInt());
		System.out.print("Enter City: ");
		address.setCity(sc.next());
		System.out.print("Enter Locality: ");
		address.setLocality(sc.next());
		System.out.print("Enter Pin Code: ");
		address.setPinCode(sc.next());
		
		System.out.print("\n\n");
		
		Employee employee = new Employee();
		System.out.print("Enter Employee ID: ");
		employee.setEmpId(sc.nextInt());
		System.out.print("Enter Name: ");
		employee.setEmpName(sc.next());
		System.out.print("Enter Employee Salary: ");
		employee.setEmpSal(sc.nextDouble());
		System.out.println("Employee Address already Entered");
		employee.setEmpAddress(address);
		
		System.out.print("\n");
		System.out.print("Output from File");
		OutputStream os = new FileOutputStream("EmployeeData.txt");
		ObjectOutputStream oos = new ObjectOutputStream(os);
		oos.writeObject(employee);
		oos.flush();
		oos.close();
		os.close();
		
		System.out.println("Employee ID: "+employee.getEmpId());
		System.out.println("Employee Name: "+employee.getEmpName());
		System.out.println("Employee Salary: "+employee.getEmpSal());
		System.out.println("Employee Address: ("+employee.getEmpAddress()+")");
		
		InputStream is = new FileInputStream("EmployeeData.txt");
		ObjectInputStream ois = new ObjectInputStream(is);
		employee =(Employee)ois.readObject();
		System.out.println(employee);
		ois.close();
		is.close();
		}catch(IOException e){
			System.out.println(e);
		}
		catch(InputMismatchException e){
			System.out.println("Please Enter Numeric Value!");
		}
		catch(ClassNotFoundException e){
			System.out.println("The Employee class Not Founded!");
		}
		finally{
			System.out.println("\nSee you and Remember Run again!");
		}
	}
}
