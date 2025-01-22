
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class GUI2 {
    public static void main(String[] args) {
        // Membuat frame
        JFrame frame = new JFrame("Aplikasi Baca File");
        frame.setSize(400, 300);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);

        // Membuat tombol
        JButton button = new JButton("Baca File");
        button.setBounds(150, 20, 100, 30);

        // Membuat area teks
        JTextArea textArea = new JTextArea();
        textArea.setBounds(50, 70, 300, 150);
        textArea.setEditable(false);

        // Menambahkan ActionListener ke tombol
        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                try {
                    // Nama file untuk dibaca (ubah sesuai lokasi file Anda)
                    String fileName = "example.txt";

                    // Membaca file
                    BufferedReader reader = new BufferedReader(new FileReader(fileName));
                    StringBuilder content = new StringBuilder();
                    String line;

                    while ((line = reader.readLine()) != null) {
                        content.append(line).append("\n");
                    }

                    reader.close();
                    textArea.setText(content.toString());
                } catch (IOException ex) {
                    textArea.setText("Error: File tidak ditemukan!");
                }
            }
        });

        // Menambahkan tombol dan area teks ke frame
        frame.add(button);
        frame.add(textArea);

        // Menampilkan frame
        frame.setVisible(true);
    }
}

    
