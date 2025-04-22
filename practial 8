# java
Practical No. 08:- Events
a)Write a program to demonstrate ActionEvent with Button Click

import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class BtnClkDemo
{
	public static void main(String[] args)
	{
	   JFrame frame=new JFrame("Button Click Demo");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   JButton button=new JButton("Click Me");
	   button.addActionListener(new ActionListener(){
	    @Override
	    public void actionPerformed(ActionEvent e){
	      JOptionPane.showMessageDialog(frame,"Button Clicked!");
	      }
	     });
	   frame.getContentPane().add(button);
	   frame.pack();
	   frame.setVisible(true);
	}
}


b)Write a program to demonstrate ActionEvent with Menu Item

import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class MenuItmClk
{
	public static void main(String[] args)
	{
	   JFrame frame=new JFrame("Menu Item Click Demo");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   JMenuBar menuBar=new JMenuBar();
	   JMenu fileMenu=new JMenu("File");
	   JMenuItem openItem=new JMenuItem("Open");
	   JMenuItem saveItem=new JMenuItem("save");
	   openItem.addActionListener(new ActionListener(){
	    @Override
	    public void actionPerformed(ActionEvent e){
	      JOptionPane.showMessageDialog(frame,"File->Open clicked!");
	      }
	     });
	    saveItem.addActionListener(new ActionListener(){
	    @Override
	    public void actionPerformed(ActionEvent e){
	      JOptionPane.showMessageDialog(frame,"File->save clicked!");
	      }
	     });
	   fileMenu.add(openItem);
	    fileMenu.add(saveItem);
	   menuBar.add(fileMenu);
	   frame.setJMenuBar(menuBar);
	   frame.setSize(400,300);
	   frame.setVisible(true);
	}
}


c)Write a program to demonstrate ActionEvent with Text Field Enter Key Event
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyEvent;
import java.awt.event.KeyListener;
public class TxtEntrKey
{
	public static void main(String[] args)
	{
	   JFrame frame=new JFrame("Text Field Enter Key Demo");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   JTextField textField=new JTextField(20);
	   textField.addActionListener(new ActionListener(){
	      @Override
	    public void actionPerformed(ActionEvent e){
	      JOptionPane.showMessageDialog(frame,"Enter key pressed in text field");
	      }
	   });
	    frame.getContentPane().add(textField);
	    frame.pack();
	    frame.setSize(400,300);
	    frame.setVisible(true);
	}
}




d)Write a program to demonstrate MouseEvents
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.MouseAdapter;
import java.awt.event.MouseEvent;
public class AllMouseEvent
{
	public static void main(String[] args)
	{
	  SwingUtilities.invokeLater(()->{
	    JFrame frame=new JFrame("Mouse Cllick Event Demo");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	    JPanel panel=new JPanel();
	    
	    JLabel j1=new JLabel();
	    panel.add(j1);
	    panel.addMouseListener(new MouseAdapter(){
	     @Override
	     public void mouseClicked(MouseEvent e){
	     JOptionPane.showMessageDialog(frame,"Mouse Clicked at("+e.getX()+","+e.getY()+")");
	      }
	   });
	    panel.addMouseMotionListener(new MouseAdapter(){
	     @Override
	     public void mouseMoved(MouseEvent e){
	    j1.setText("Mouse moved at("+e.getX()+","+e.getY()+")");
	      }
	   });
	     panel.addMouseListener(new MouseAdapter(){
	     @Override
	     public void mouseEntered(MouseEvent e){
	     frame.setTitle("Mouse Entered");
	      }
	     @Override
	     public void mouseExited(MouseEvent e){
	     frame.setTitle("Mouse Exited");
	      }
	   });
	    frame.add(panel);
	    frame.pack();
	    frame.setSize(400,300);
	    frame.setVisible(true);
	  });
	}
}


e)Write a program to demonstrate KeyEvents
import javax.swing.*;
import java.awt.event.*;
public class AllKeyEvents
{
	public static void main(String[] args)
	{
	   JFrame frame=new JFrame("All key Events");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   JTextField textField=new JTextField(20);
	   frame.add(textField);
	   textField.addKeyListener(new KeyAdapter(){
	    @Override
	    public void keyTyped(KeyEvent e){
	     System.out.println("Key Typed:"+e.getKeyChar());
	    }
	    @Override
	    public void keyPressed(KeyEvent e){
	     System.out.println("Key Pressed:"+KeyEvent.getKeyText(e.getKeyCode()));
	    }
	    @Override
	    public void keyReleased(KeyEvent e){
	     System.out.println("Key Released:"+KeyEvent.getKeyText(e.getKeyCode()));
	    }
	   });
	   frame.pack();
	   frame.setVisible(true);
	}
}


f)Write a program to demonstrate SelectionEvent

import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class SelectionEvents
{
	public static void main(String[] args)
	{
	   SwingUtilities.invokeLater(()->{
	   JFrame frame=new JFrame("Selection Event Demo");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   String[] items={"item1","item2","item3"};
	   JComboBox<String> comboBox=new JComboBox<>(items);
	   comboBox.addActionListener(new ActionListener()
	   {
		@Override
		public void actionPerformed(ActionEvent e)
		{
		 String selectedItem=(String) comboBox.getSelectedItem();
		 System.out.println("Selected:"+selectedItem);
		}
	    });
	    frame.add(comboBox,BorderLayout.CENTER);
	    frame.setSize(300,200);
	    frame.setVisible(true);
	   });
	}
}


g)Write a program to demonstrate FocusEvent
import javax.swing.*;
import java.awt.*;
import java.awt.event.FocusEvent;
import java.awt.event.FocusListener;
public class AllFocusEvents
{
	public static void main(String[] args)
	{
	   SwingUtilities.invokeLater(()->{
	   JFrame frame=new JFrame("Focus Event");
	   frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	   JPanel panel=new JPanel();
	   panel.setPreferredSize(new Dimension(300,200));
	   JLabel label=new JLabel();
	   JTextField textField1=new JTextField(25);
	   JTextField textField2=new JTextField(25);
	   textField1.addFocusListener(new FocusListener()
	   {
	     @Override
	     public void focusGained(FocusEvent e)
	     {
		label.setText("Focus Gained");
	     }
	     @Override
	     public void focusLost(FocusEvent e)
	     {
		label.setText("Focus Lost");
	     }
	   });
	   panel.add(label);
	   panel.add(textField1);
	   panel.add(textField2);
	   frame.add(panel);
	   frame.setVisible(true);
	  });
	}
}
