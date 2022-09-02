# bank.java
This is an bank project for college student 

package lib;
//import java.util.jar.JarOutputStream;
import javax.swing.JFrame;
import javax.swing.JOptionPane;
//import javax.xml.stream.events.StartDocument;
 class Calculater {
        public static double a,b;
        public static double result;
    public static void main(String[] args) {
     //   JOptionPane.showMessageDialog(null,"WELCOME SWARNIL  RAJ,  WHAT DO YOU WANT ");
        input();
    }
    public static void  input(){
        JFrame ob;
        ob = new JFrame();
    String first_digit = JOptionPane.showInputDialog(ob,"ENTER YOUR FIRST NUMBER ");
        a=Integer.parseInt(first_digit);
        String second_digit=JOptionPane.showInputDialog(ob,"ENTER YOUR SECOND NUMBER");
        b=Integer.parseInt(second_digit);
        optionMsCollege();   }
    public static void optionMsCollege(){
        JFrame oob= new JFrame();
        String  opti= JOptionPane.showInputDialog(oob,"ENTER YOUR OPTION \n 1. ADDITION \n 2. SUBSTRACTION \n 3. MULTIPLICATION \n 4. DIVISION \n 5. RESTART ");
       int op =Integer.parseInt(opti);
        switch(op)
        {
           case 1:
           JOptionPane.showMessageDialog(oob,"********** ADDITION **********");
           add();
           break;
            case 2:
            JOptionPane.showMessageDialog(oob,"******** SUBSTRACTION ********");
          substraction();
            break;
            case 3:
            JOptionPane.showMessageDialog(oob,"********* MULTIPLICATION *********");
            multiplication();
            break;
            case 4:
            JOptionPane.showMessageDialog(oob,"**********  DIVISION **********");
            division();
            break;
            case 5:
            start();
            default:
            JOptionPane.showMessageDialog(oob,"INVAILD INPUT, TRY AGAIN ");
            optionMsCollege();
            break;
        }
    }
    public static void add(){
        JFrame o=new JFrame();
        result= a+b;
        JOptionPane.showMessageDialog(o,"RESULT = "+result);
       // Icon or;
       // JOptionPane.showConfirmDialog(o,"YOU WANT TO PROFERM  MORE OPERATION ","ALEART",YES_NO_OPTION);
       String opt= JOptionPane.showInputDialog(o,"YOU WANT TO PROFERM MORE OPE0 RATION \n .  YES \n .  NO \n . RESTART");
       
    if(opt.equals("yes") || opt.equals("YES")){
           OptionAgainMsCollege();
       }if (opt.equals("RESTART") || opt.equals("restart")){
           start();
       }else{
           JOptionPane.showMessageDialog(o,"THANK YOU ");
           System.exit(0);
       }    
    }
    public static void substraction(){
        JFrame op=new JFrame();
        result =a-b;
        JOptionPane.showMessageDialog(op,"RESULT"+result);
        String opR=JOptionPane.showInputDialog(op,"YOU WANT TO PROFERM  MORE OPERATION \n .  YES \n .  NO");
        
        if(opR.equals("YES") || opR.equals("yes"))
        {
            OptionAgainMsCollege();
                }if(opR.equals ("restart")|| opR.equals("RESTART")){
            start();
        }
        else{
            JOptionPane.showMessageDialog(op,"THANK YOU  ");
            System.exit(0);
        }
    }
    public static void division(){
        JFrame o_p= new JFrame();
          result= a/b;
        JOptionPane.showMessageDialog(o_p,"RESULT ="+result); 
        String oo = JOptionPane.showInputDialog(o_p,"WANT TO PROFORM  MORE OPERATION \n .  YES \n .  NO");
        if(oo.equals("yes") || oo.equals("YES")){
            OptionAgainMsCollege();
        }if(oo.equals("restart")|| oo.equals("RESTART")){
            start();
        }
        else{
            JOptionPane.showMessageDialog(o_p,"THANK YOU");
            System.out.println(0);
        }
    }
    public static void multiplication(){
        JFrame O_p = new JFrame();
        result =a*b;
        JOptionPane.showMessageDialog(O_p,"RESULT = "+result);
//        option_again();
        JOptionPane.showMessageDialog(O_p,"DO ANOTHER OPERATION \n . YES \n . NO . \n . RESTART");
        if(O_p.equals("yes") || O_p.equals("YES")){
            OptionAgainMsCollege();
        }if(O_p.equals("RESTART")|| O_p.equals("restart")){
            start();
        }else{
            JOptionPane.showMessageDialog(O_p,"THANK YOU ");
            System.exit(0);
        }
    }
    public static void OptionAgainMsCollege(){
        JFrame oo=new JFrame();
       String OPTICAL= JOptionPane.showInputDialog(oo,"ENTER YOUR OPTION \n 1. ADD \n 2. SUBSTRACTION \n 3. DIVISION \n 4. MULTIPLICATION \n 5. RESTART");
       int option = Integer.parseInt(OPTICAL);
       String numb=  JOptionPane.showInputDialog(oo,"ENTER YOUR NUMBER ");
        double rr= Double.parseDouble(numb);
       String o;
       switch( option)
       {
           case 1:
           result=rr+result;
           JOptionPane.showMessageDialog(oo,"RESULT ="+result);
           o=JOptionPane.showInputDialog(oo,"DO ANOTHER OPERATION \n .  YES \n .  NO \n RESTART");
           if(o.equals("yes") || o.equals("YES"))
           {
               OptionAgainMsCollege();
           }if(o.equals("restart")|| o.equals("RESTART")){
               start();
           }
           else {
               JOptionPane.showMessageDialog(oo,"THANK YOU ");
               System.exit(0);
           }
           break;
        case 2:
           result= rr-result;
           JOptionPane.showMessageDialog(oo,"RESULT="+result);
           o=JOptionPane.showInputDialog(oo,"WANT TO  PERFOEM MORE  OPERATION \n .  YES .  \n  NO \n RESTART");
           if(o.equals("YES") || o.equals("yes"))
           {
               OptionAgainMsCollege();
           }if(o.equals("restart")|| o.equals("RESTART")){
            start();
        }
           else{
               JOptionPane.showMessageDialog(oo,"THANK YOU");
               System.exit(0);
           }
           break;
           case 3:
           result=rr/result;
           JOptionPane.showMessageDialog(oo,"RESULT ="+result);
           o=JOptionPane.showInputDialog(oo,"WANT TO PERFORM MORE OPERATION \n .  YES \n .  NO \n RESTART");
           if(o.equals("yes") || o.equals("YES")){
               OptionAgainMsCollege();
           }if(o.equals("restart")|| o.equals("RESTART")){
            start();
        }
           else{
               JOptionPane.showMessageDialog(oo,"THANK YOU ");
               System.exit(0);
           }
           break;
           case 4:
           result= rr*result;
           JOptionPane.showMessageDialog(oo,"RESULT ="+result);
           o=JOptionPane.showInputDialog(oo,"WANT TO PROFORM MORE OPERATION \n .  YES \n .  NO \n RESTART");
           if(o.equals("YES")|| o.equals("yes"))
           {
               OptionAgainMsCollege();
                       }if(o.equals("restart")|| o.equals("RESTART")){
            start();
        }
           else{
               JOptionPane.showMessageDialog(oo,"THANK YOU ");
               System.exit(0);
              }
           break;
           case 5:
           start();
           break;
           default:
           JOptionPane.showMessageDialog(oo,"SORRY WE'CAN'T  PERFORM THIS OPERATION ");
           optionMsCollege();
           break;
       }
    }
    public static void start(){
        result=0;
        input();  }
}

