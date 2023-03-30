package swing_project;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import java.awt.Color;
import javax.swing.JLabel;
import javax.swing.JTextField;
import java.awt.Font;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class calculator extends JFrame {

	private JPanel contentPane;
	private JTextField t1;
	private JTextField t2;
	private JTextField t3;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					calculator frame = new calculator();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the frame.
	 */
	public calculator() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 450, 300);
		contentPane = new JPanel();
		contentPane.setBackground(new Color(128, 0, 128));
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));

		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		JLabel lb1 = new JLabel("CALCULATOR");
		lb1.setForeground(new Color(0, 255, 0));
		lb1.setFont(new Font("Tahoma", Font.BOLD, 18));
		lb1.setBackground(new Color(240, 240, 240));
		lb1.setBounds(163, 21, 119, 22);
		contentPane.add(lb1);
		
		JLabel lb2 = new JLabel("Enter first number");
		lb2.setForeground(new Color(255, 255, 255));
		lb2.setFont(new Font("Tahoma", Font.BOLD, 14));
		lb2.setBounds(72, 60, 127, 17);
		contentPane.add(lb2);
		
		t1 = new JTextField();
		t1.setFont(new Font("Tahoma", Font.BOLD, 14));
		t1.setBounds(241, 60, 168, 28);
		contentPane.add(t1);
		t1.setColumns(10);
		
		JLabel lb3 = new JLabel("Enter second number");
		lb3.setForeground(Color.WHITE);
		lb3.setFont(new Font("Tahoma", Font.BOLD, 14));
		lb3.setBounds(72, 105, 149, 17);
		contentPane.add(lb3);
		
		t2 = new JTextField();
		t2.setFont(new Font("Tahoma", Font.BOLD, 14));
		t2.setColumns(10);
		t2.setBounds(241, 105, 168, 29);
		contentPane.add(t2);
		
		JButton b2 = new JButton("SUB");
		b2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String data1=t1.getText();
				String data2=t2.getText();
				int val1=Integer.valueOf(data1);
				int val2=Integer.valueOf(data2);
				int res=val1-val2;
				String result=String.valueOf(res);
				t3.setText(result);
			}
		});
		b2.setForeground(new Color(128, 0, 0));
		b2.setFont(new Font("Tahoma", Font.BOLD, 14));
		b2.setBounds(133, 206, 69, 29);
		contentPane.add(b2);
		
		JButton b3 = new JButton("MUL");
		b3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String data1=t1.getText();
				String data2=t2.getText();
				int val1=Integer.valueOf(data1);
				int val2=Integer.valueOf(data2);
				int res=val1*val2;
				String result=String.valueOf(res);
				t3.setText(result);
			}
			
		});
		b3.setForeground(new Color(128, 0, 0));
		b3.setFont(new Font("Tahoma", Font.BOLD, 14));
		b3.setBounds(230, 206, 69, 29);
		contentPane.add(b3);
		
		JButton b4 = new JButton("DIV");
		b4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String data1=t1.getText();
				String data2=t2.getText();
				float val1=Float.valueOf(data1);
				float val2=Float.valueOf(data2);
				float res=val1/val2;
				String result=String.valueOf(res);
				t3.setText(result);
			}
			
		});
		b4.setForeground(new Color(128, 0, 0));
		b4.setFont(new Font("Tahoma", Font.BOLD, 14));
		b4.setBounds(329, 206, 69, 29);
		contentPane.add(b4);
		
		JLabel lb4 = new JLabel("RESULT");
		lb4.setForeground(Color.WHITE);
		lb4.setFont(new Font("Tahoma", Font.BOLD, 16));
		lb4.setBounds(72, 154, 149, 17);
		contentPane.add(lb4);
		
		t3 = new JTextField();
		t3.setFont(new Font("Tahoma", Font.BOLD, 14));
		t3.setColumns(10);
		t3.setBounds(241, 148, 168, 29);
		contentPane.add(t3);
		
		JButton b1 = new JButton("ADD");
		b1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				String data1=t1.getText();
				String data2=t2.getText();
				int val1=Integer.valueOf(data1);
				int val2=Integer.valueOf(data2);
				int res=val1+val2;
				String result=String.valueOf(res);
				t3.setText(result);
			}
		});
		b1.setForeground(new Color(128, 0, 0));
		b1.setFont(new Font("Tahoma", Font.BOLD, 14));
		b1.setBounds(28, 206, 69, 29);
		contentPane.add(b1);
	}
}
