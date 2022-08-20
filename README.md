import javax.swing.*;  
import javax.swing.JPanel;

import java.awt.BorderLayout;
import java.awt.Color;
import java.awt.Container;

import javax.swing.ImageIcon;
import javax.swing.JFrame;
import javax.swing.JLabel;
import java.util.Scanner;
public class MyProgram extends JFrame{
    
    
    JFrame f;
    private double weight; 
    private double height;
    
    public static void main(String[] args) {
        new MyProgram();
    }
    
    
    
    
    MyProgram() {
        
        f=new JFrame();
        f.setTitle("BMI Calculator");
        f.setSize(1000,1000);
        f.setVisible(true);
        f.getContentPane().setBackground(Color.BLUE);
        
         //JButton button = new JButton("click me");
       // button.setBounds(50,55,55,55);
        //  f.add(button);
       // button.setSize(100,100);
        boolean condition = false;
        while(!false){
            JOptionPane.showMessageDialog(null, "Welcome to the Body Mass Index Calculator","WELCOME",1);
            
            this.weight = Double.parseDouble(JOptionPane.showInputDialog(null,"Hello! Input your Weight in kilograms"));
            
            
            this.height = Double.parseDouble(JOptionPane.showInputDialog(null,"Hello! Input your Height in centimeters"));
            
            double heightMeter = this.height/100; //get meters
            
            double BMI = weight/(heightMeter*heightMeter);
            
            JOptionPane.showMessageDialog(null,  String.format("Your Body Mass Index is %.2f",  BMI));
            
            if(BMI < 18.5){
                JOptionPane.showMessageDialog(null, "You are underweight");
                JOptionPane.showMessageDialog(null, "Eat more frequently. Because you will feel full faster, eat as much as you can. \nEat smaller meals during the day and not large meals like lunch and dinner");
            }
            else if(18.5 <= BMI && BMI <= 24.9){
                JOptionPane.showMessageDialog(null, "You are Normal. Congratulations!");
                JOptionPane.showMessageDialog(null, "Make sure to keep a healthy lifestyle like you're doing");
            }
            else if(25 <= BMI && BMI <= 29.9){
                JOptionPane.showMessageDialog(null, "You are Overweight");
                JOptionPane.showMessageDialog(null, "Track your progress using online food or physical activity trackers that \ncan help you keep track of the foods you eat, your physical activity, and your weight.\n These tools may help you stick with it and stay motivated.");
            } 
            else{
                JOptionPane.showMessageDialog(null, "You are Obese");
                JOptionPane.showMessageDialog(null, "You need to set specific goals can help you stay on track. Rather than \nbeing more active, set a goal to excercise or play a sport\n 15 to 30 minutes before work or at lunch on Monday and Friday.");
            }
        }
    }
    
    
        // if BMI < 18.5 == underweight
        //else if BMI  18.5-24.9: Normal
        //else if BMI 25-29.9: Overweight
        //else: Obese
    
}
