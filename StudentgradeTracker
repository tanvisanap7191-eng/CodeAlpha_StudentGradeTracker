import java.util.ArrayList;
import java.util.Scanner;

class Student
{
    String name;
    double marks;

    Student(String name,double marks)
    {
        this.name=name;
        this.marks=marks;
    }

    void display()
    {
        System.out.println("----------------");
        System.out.println("Name:"+name);
        System.out.println("Marks:"+marks);
    }

}

public class StudentGradeTracker
{
    ArrayList<Student> students=new ArrayList<>();

    public void addStudent(Student s)
    {
        students.add(s);
    }

    public void displayStudent()
    {
        try {
            if(students.isEmpty())
            {
                throw new Exception("Students Record Not found.");
            }
            for(int i=0;i<students.size();i++)
            {
                Student s=students.get(i);
                s.display();
            }
            
        } catch (Exception e) {
            System.out.println("Error:"+e.getMessage());
        }
    }

    public double calculateAverage()
    {
        if(students.isEmpty())
        {
            System.err.println("Error:Student not found");
            return 0;
        }
        double total=0;
        for(int i=0;i<students.size();i++)
        {
            total+=students.get(i).marks;

        }
        double average=total/students.size();
        System.out.println("Average:"+average);
        return average;
    }
    public void highestMarks()
    {
        if(students.isEmpty())
        {
            System.err.println("Error:Student not found");
            return;
        }

        Student highest=students.get(0);
        for(int i=0;i<students.size();i++)
        {
            if(students.get(i).marks>highest.marks)
            {
                highest=students.get(i);
            }
            
        }
        System.out.println("Highest marks:");
        highest.display();
    }
     public void lowestMarks()
    {
        if(students.isEmpty())
        {
            System.err.println("Error:Student not found");
            return;
        }

        Student lowest=students.get(0);
        for(int i=0;i<students.size();i++)
        {
            if(students.get(i).marks<lowest.marks)
            {
                lowest=students.get(i);
            }
            
        }
        System.out.println("lowest marks:");
        lowest.display();
    }
    
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        StudentGradeTracker tracker = new StudentGradeTracker();

        System.out.print("Enter number of students: ");
        int n = sc.nextInt();
        sc.nextLine();

        for (int i= 0; i<n;i++) {
            System.out.print("Enter Name:");
            String name=sc.nextLine();

            System.out.print("Enter marks:");
            double marks=sc.nextDouble();
            sc.nextLine();

            tracker.addStudent(new Student(name, marks));
            
        }
        System.out.println("\n====STUDENT SUMMARY REPORT====");

        tracker.displayStudent();
        System.out.println();

        tracker.calculateAverage();
        System.out.println();

        tracker.highestMarks();
        System.out.println();

        tracker.lowestMarks();
        System.out.println();

        sc.close();

    }
}