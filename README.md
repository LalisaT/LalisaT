/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */

import javax.microedition.midlet.*;
import javax.microedition.lcdui.*;
/**
 * @author user
 */
public class CalculatorMidlet extends MIDlet implements CommandListener
{
    private Display d;
    private Form f;
    private TextField tf1,tf2;
    private ChoiceGroup cg;
    private StringItem si;
    private Command exit,calculate;
    private int a,s,m,div;


    public CalculatorMidlet()
    {
        d=Display.getDisplay(this);
        f=new Form("Calculator");


        exit=new Command("Exit",Command.EXIT,0);
        calculate=new Command("Calculate",Command.SCREEN,0);
        f.addCommand(exit);
        f.addCommand(calculate);
        f.setCommandListener(this);


        tf1=new TextField("Number1","",4,TextField.NUMERIC);
        




