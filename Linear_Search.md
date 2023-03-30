```java

package projects;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import java.awt.Color;
import javax.swing.JLabel;
import javax.swing.JTextField;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class LinearSearch extends JFrame {

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
					LinearSearch frame = new LinearSearch();
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
	public LinearSearch() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 450, 300);
		contentPane = new JPanel();
		contentPane.setBackground(new Color(128, 0, 0));
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));

		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		JLabel lb1 = new JLabel("LINEAR SEARCH");
		lb1.setForeground(new Color(255, 255, 255));
		lb1.setFont(new Font("Tahoma", Font.BOLD, 17));
		lb1.setBounds(144, 11, 144, 14);
		contentPane.add(lb1);
		
		JLabel lb2 = new JLabel("Enter numbers");
		lb2.setForeground(new Color(255, 255, 255));
		lb2.setFont(new Font("Tahoma", Font.BOLD, 14));
		lb2.setBounds(37, 43, 120, 20);
		contentPane.add(lb2);
		
		t1 = new JTextField();
		t1.setFont(new Font("Tahoma", Font.BOLD, 14));
		t1.setBounds(223, 43, 173, 32);
		contentPane.add(t1);
		t1.setColumns(10);
		
		JButton btn = new JButton("SEARCH");
		btn.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				 String[] inputArr = t1.getText().split(" ");
			        int[] arr = new int[inputArr.length];

			        for (int i = 0; i < inputArr.length; i++) {
			            arr[i] = Integer.parseInt(inputArr[i]);
			        }
			        String searchVal = t2.getText();
			        int var=Integer.valueOf(searchVal);
			        int index = -1;

			        for (int i = 0; i < arr.length; i++) {
			            if (arr[i] == var) {
			                index = i;
			                break;
			            }
			        }
			        
			        
			        if (index == -1) {
			            t3.setText(searchVal + " not found in the array.");
			        } else {
			            t3.setText(searchVal + " found at index " + index + " in the array.");
			        }


			}
		});
		btn.setFont(new Font("Tahoma", Font.BOLD, 16));
		btn.setBounds(159, 213, 144, 23);
		contentPane.add(btn);
		
		JLabel lb3 = new JLabel("Enter key to search");
		lb3.setForeground(Color.WHITE);
		lb3.setFont(new Font("Tahoma", Font.BOLD, 14));
		lb3.setBounds(37, 94, 144, 20);
		contentPane.add(lb3);
		
		JLabel lb4 = new JLabel("Result");
		lb4.setForeground(Color.WHITE);
		lb4.setFont(new Font("Tahoma", Font.BOLD, 14));
		lb4.setBounds(37, 147, 120, 20);
		contentPane.add(lb4);
		
		t2 = new JTextField();
		t2.setFont(new Font("Tahoma", Font.BOLD, 14));
		t2.setColumns(10);
		t2.setBounds(223, 96, 173, 32);
		contentPane.add(t2);
		
		t3 = new JTextField();
		t3.setFont(new Font("Tahoma", Font.BOLD, 14));
		t3.setColumns(10);
		t3.setBounds(112, 147, 284, 32);
		contentPane.add(t3);
	}
}

```
