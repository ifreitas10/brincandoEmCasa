# brincandoEmCasa

import javax.swing.*;

public class estudoProva {
    public static String calcular(int num1, int num2){
        int somar = 0;
        int subtrair = 0;
        int multiplicar = 0;
        int dividir = 0;

        String valorDoSwitch = (JOptionPane.showInputDialog("1- SOMAR | 2- SUBTRAIR | 3- MULTIPLICAR | 4- DIVIDIR"));

        switch(valorDoSwitch){
            case "1":
                somar = (num1+num2);
                JOptionPane.showMessageDialog(null,"Soma dos valores recebidos: "+somar);
                break;
            case "2":
                subtrair = (num1-num2);
                JOptionPane.showMessageDialog(null,"Subtração dos valores recebidos: "+subtrair);
                break;
            case "3":
                multiplicar = (num1*num2);
                JOptionPane.showMessageDialog(null,"Multiplicação dos valores recebidos: "+multiplicar);
                break;
            case "4":
                dividir = (num1/num2);
                JOptionPane.showMessageDialog(null,"Divisão dos valores recebidos: "+dividir);
                break;
            default:
                JOptionPane.showMessageDialog(null,"Operação recebida não identificada");
                break;
        }
        return valorDoSwitch;

    }
    public static void menuPrograma(){
        String respostaUsuario = JOptionPane.showInputDialog("Deseja continuar? SIM/NAO");

        if (respostaUsuario.equals("SIM")){
            meuProgramaInteiro();
        }else{
            JOptionPane.showMessageDialog(null,"Saiu");
        }
    }
    public static void meuProgramaInteiro(){
        int num1 = Integer.parseInt(JOptionPane.showInputDialog("Digite um inteiro"));
        int num2 = Integer.parseInt(JOptionPane.showInputDialog("Digite um inteiro"));
        calcular(num1,num2);
        menuPrograma();
    }

    public static void main(String[] args){
        meuProgramaInteiro();
    }
}
