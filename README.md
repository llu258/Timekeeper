# Timekeeper
This is the timekeeper Java program that we made using the Netbeans App.



About the program:
This timekeeper program we build was widely used in schools, offices, factories, and other professional buildings.

The program used an identification system (ID) thus whenever we scan our ID the program will record the following:

picture of the ID
your name
date,
and time of entering the establishment
isn’t it cool right? Share lang namin…😁👍

Into the program:


N O T E :
jTextfield1 – Student Number / ID Number
jTextfield2 – Student Name
jTextfield3 – Date
jTextfield4 – Time
jButton1. – Log in
jLabel1. – Picture
jLabel2. – Current Time
jLabel3. – Current Date
CODE:

public class cTimeKeeper extends javax.swing.JFrame {

Timer timer;

public cTimeKeeper() {

initComponents();

setLocationRelativeTo(null);

ActionListener actionListener = new ActionListener(){

public void actionPerformed(ActionEvent e) {

Date date = new Date();

DateFormat timeFormat = new SimpleDateFormat(“HH:mm:ss”);

DateFormat dateFormat = new SimpleDateFormat(“MMMMMMMMMM dd, yyyy”);

String time = timeFormat.format(date);

String day = dateFormat.format(date);


jLabel2.setText(time);

jLabel3.setText(day);

}

};

timer = new Timer(1000,actionListener);

timer.setInitialDelay(0);

timer.start();

}

private void jTextField1ActionPerformed(java.awt.event.ActionEvent evt) {

jTextField2.setText(“Jesus Luigi M. Sison”);

jTextField3.setText(jLabel3.getText());

jTextField4.setText(jLabel2.getText());

jLabel8.setIcon(new javax.swing.ImageIcon(getClass().getResource(“1.jpg”)));

jButton1.setEnabled(true);

}

private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {

String msg = “Student No:”+jTextField1.getText()+”\n”+

“Student Name:”+jTextField2.getText()+”\n”+

“Date:”+jTextField3.getText()+”\n”+”Time In:”+

jTextField4.getText();

JOptionPane.showMessageDialog(null,msg);

jTextField1.setText(“”);

jTextField2.setText(“”);

jTextField3.setText(“”);

jTextField4.setText(“”);

jButton1.setEnabled(false);

}

private void jTextField3ActionPerformed(java.awt.event.ActionEvent evt) {

// TODO add your handling code here:

}

private void jTextField4ActionPerformed(java.awt.event.ActionEvent evt) {

// TODO add your handling code here:

}

public static void main(String args[]) {

/* Set the Nimbus look and feel */

//<editor-fold defaultstate=”collapsed” desc=” Look and feel setting code (optional) “>

/* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.

* For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html

*/

try {

for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {

if (“Nimbus”.equals(info.getName())) {

javax.swing.UIManager.setLookAndFeel(info.getClassName());

break;

}

}

} catch (ClassNotFoundException ex) {

java.util.logging.Logger.getLogger(cTimeKeeper.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);

} catch (InstantiationException ex) {

java.util.logging.Logger.getLogger(cTimeKeeper.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);

} catch (IllegalAccessException ex) {

java.util.logging.Logger.getLogger(cTimeKeeper.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);

} catch (javax.swing.UnsupportedLookAndFeelException ex) {

java.util.logging.Logger.getLogger(cTimeKeeper.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);

}

//</editor-fold>

/* Create and display the form */

java.awt.EventQueue.invokeLater(new Runnable() {

public void run() {

new cTimeKeeper().setVisible(true);

}

});

}

Reference:


About our reference, the program for the cTimeKeeper was made use by using NetBeans App, an application wherein you can code the site for Java Applications.
