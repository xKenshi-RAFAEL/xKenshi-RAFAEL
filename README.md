import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class DinoGame extends JPanel implements ActionListener, KeyListener {

    // Variable para almacenar el color actual del dinosaurio
    private Color dinoColor = Color.BLACK;

    // Timer para la animación
    Timer timer = new Timer(20, this);

    // Constructor
    public DinoGame() {
        this.setFocusable(true);
        this.addKeyListener(this);
        timer.start();
    }

    // Dibujar el dinosaurio y otros elementos del juego
    @Override
    public void paintComponent(Graphics g) {
        super.paintComponent(g);
        
        // Fondo
        g.setColor(Color.WHITE);
        g.fillRect(0, 0, getWidth(), getHeight());
        
        // Dino
        g.setColor(dinoColor);
        g.fillRect(50, 150, 50, 50);  // Posición del dinosaurio
    }

    // Actualización del juego
    @Override
    public void actionPerformed(ActionEvent e) {
        repaint();
    }

    // Método para cambiar el color del dinosaurio
    public void changeDinoColor(String color) {
        switch (color.toLowerCase()) {
            case "rojo":
                dinoColor = Color.RED;
                break;
            case "verde":
                dinoColor = Color.GREEN;
                break;
            case "negro":
                dinoColor = Color.BLACK;
                break;
            case "blanco":
                dinoColor = Color.WHITE;
                break;
            case "azul":
                dinoColor = Color.BLUE;
                break;
            case "rosa":
                dinoColor = Color.PINK;
                break;
            case "morado":
                dinoColor = new Color(128, 0, 128); // Color morado
                break;
            case "dorado":
                dinoColor = new Color(255, 215, 0); // Color dorado
                break;
            case "amarillo":
                dinoColor = Color.YELLOW;
                break;
            case "plata":
                dinoColor = new Color(192, 192, 192); // Color plata
                break;
            default:
                dinoColor = Color.BLACK;
                break;
        }
        repaint();
    }

    // Manejo de teclas
    @Override
    public void keyPressed(KeyEvent e) {
        if (e.getKeyCode() == KeyEvent.VK_SPACE) {
            // Acción de saltar
        }
    }

    @Override
    public void keyReleased(KeyEvent e) {}

    @Override
    public void keyTyped(KeyEvent e) {}

    // Método principal
    public static void main(String[] args) {
        JFrame frame = new JFrame("Dino Game");
        DinoGame game = new DinoGame();
        frame.add(game);
        frame.setSize(800, 400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);

        // Crear menú para cambiar el color del dinosaurio
        JMenuBar menuBar = new JMenuBar();
        JMenu colorMenu = new JMenu("Cambiar Color del Dino");
        
        String[] colors = {"Rojo", "Verde", "Negro", "Blanco", "Azul", "Rosa", "Morado", "Dorado", "Amarillo", "Plata"};
        for (String color : colors) {
            JMenuItem menuItem = new JMenuItem(color);
            menuItem.addActionListener(new ActionListener() {
                public void actionPerformed(ActionEvent e) {
                    game.changeDinoColor(color);
                }
            });
            colorMenu.add(menuItem);
        }

        menuBar.add(colorMenu);
        frame.setJMenuBar(menuBar);
    }
}import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class DinoGame extends JPanel implements ActionListener, KeyListener {

    // Variable para almacenar el color actual del dinosaurio
    private Color dinoColor = Color.BLACK;

    // Timer para la animación
    Timer timer = new Timer(20, this);

    // Constructor
    public DinoGame() {
        this.setFocusable(true);
        this.addKeyListener(this);
        timer.start();
    }

    // Dibujar el dinosaurio y otros elementos del juego
    @Override
    public void paintComponent(Graphics g) {
        super.paintComponent(g);
        
        // Fondo
        g.setColor(Color.WHITE);
        g.fillRect(0, 0, getWidth(), getHeight());
        
        // Dino
        g.setColor(dinoColor);
        g.fillRect(50, 150, 50, 50);  // Posición del dinosaurio
    }

    // Actualización del juego
    @Override
    public void actionPerformed(ActionEvent e) {
        repaint();
    }

    // Método para cambiar el color del dinosaurio
    public void changeDinoColor(String color) {
        switch (color.toLowerCase()) {
            case "rojo":
                dinoColor = Color.RED;
                break;
            case "verde":
                dinoColor = Color.GREEN;
                break;
            case "negro":
                dinoColor = Color.BLACK;
                break;
            case "blanco":
                dinoColor = Color.WHITE;
                break;
            case "azul":
                dinoColor = Color.BLUE;
                break;
            case "rosa":
                dinoColor = Color.PINK;
                break;
            case "morado":
                dinoColor = new Color(128, 0, 128); // Color morado
                break;
            case "dorado":
                dinoColor = new Color(255, 215, 0); // Color dorado
                break;
            case "amarillo":
                dinoColor = Color.YELLOW;
                break;
            case "plata":
                dinoColor = new Color(192, 192, 192); // Color plata
                break;
            default:
                dinoColor = Color.BLACK;
                break;
        }
        repaint();
    }

    // Manejo de teclas
    @Override
    public void keyPressed(KeyEvent e) {
        if (e.getKeyCode() == KeyEvent.VK_SPACE) {
            // Acción de saltar
        }
    }

    @Override
    public void keyReleased(KeyEvent e) {}

    @Override
    public void keyTyped(KeyEvent e) {}

    // Método principal
    public static void main(String[] args) {
        JFrame frame = new JFrame("Dino Game");
        DinoGame game = new DinoGame();
        frame.add(game);
        frame.setSize(800, 400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);

        // Crear menú para cambiar el color del dinosaurio
        JMenuBar menuBar = new JMenuBar();
        JMenu colorMenu = new JMenu("Cambiar Color del Dino");
        
        String[] colors = {"Rojo", "Verde", "Negro", "Blanco", "Azul", "Rosa", "Morado", "Dorado", "Amarillo", "Plata"};
        for (String color : colors) {
            JMenuItem menuItem = new JMenuItem(color);
            menuItem.addActionListener(new ActionListener() {
                public void actionPerformed(ActionEvent e) {
                    game.changeDinoColor(color);
                }
            });
            colorMenu.add(menuItem);
        }

        menuBar.add(colorMenu);
        frame.setJMenuBar(menuBar);
    }
}
