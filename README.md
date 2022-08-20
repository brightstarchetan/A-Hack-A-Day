# A-Hack-A-Day
Project for A Hack A Day Hackathon

import javax.swing.*;  
import java.util.Scanner;
public class MyProgram {
    JFrame f;
    private double weight; 
    private double height;
    MyProgram() {
        f=new JFrame();
        
        this.weight = Double.parseDouble(JOptionPane.showInputDialog(null,"Hello! Input your Weight in kilograms"));
        
        
        this.height = Double.parseDouble(JOptionPane.showInputDialog(null,"Hello! Input your Height in centimeters"));
        
        double heightMeter = this.height/100; //get meters
        
        double BMI = weight/(heightMeter*heightMeter);
        
        JOptionPane.showMessageDialog(null,  String.format("Your BMI is %.2f",  BMI));
        
        if(BMI < 18.5){
            JOptionPane.showMessageDialog(null, "You are underweight");
        }
        else if(18.5 <= BMI && BMI <= 24.9){
            JOptionPane.showMessageDialog(null, "You are Normal. Congratulations!");
        }
        else if(25 <= BMI && BMI <= 29.9){
            JOptionPane.showMessageDialog(null, "You are Overweight");
        } 
        else{
            JOptionPane.showMessageDialog(null, "You are Obese");
        }
    }
    
    
    
        // if BMI < 18.5 == underweight
        //else if BMI  18.5-24.9: Normal
        //else if BMI 25-29.9: Overweight
        //else: Obese
    public static void main(String[] args) {
        new MyProgram();
    }
}
