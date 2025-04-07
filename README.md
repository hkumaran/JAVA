# JAVA
Codes for java program
01> NATWEST INTERVIEW QUESTION
int[] arr={21,23,43,56,21} in this array reverse each array lement and find the duplicates if exists.

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.HashSet;
class Main {
    public static void main(String[] args) {
        int[] arr={12,23,34,45,23};
        System.out.println("Try programiz.pro");
        for(int x:arr)
        {
            System.out.println(reverselogic(x));
        }
        System.out.println("Duplicates : "+findduplicate(arr));
    }
    public static int reverselogic(int num)
    {
        int rev=0;
        while(num!=0)
        {
        int lastdigit=num%10;
        rev=rev*10+lastdigit;
        num=num/10;
        }
        return rev;
    }
    public static boolean findduplicate(int[] z)
    {
        HashSet<Integer> set=new HashSet<>();
        for(int q:z)
        {
            if(set.contains(q))
            {
                System.out.println("Duplicates Found"+q);
                return true;
            }
            set.add(q);
        }
        return false;
    }
}
