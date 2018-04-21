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
-----------------------------------------------------------------------------------------------------------


//Calculo para mostrar as combinações possíveis de 2 dados com 6 valores em cada.
    public static void calcularDados(int dadoUm, int dadoDois){
        for (dadoUm =1; dadoUm <= 6; dadoUm++){
            for(dadoDois= 1; dadoDois<=6; dadoDois++){
                System.out.print("Dado1 Dado2\n  "+dadoUm+"     "+dadoDois+"\n");
                //System.out.println("Dado2\n"+dadoDois);
            }
        }
    }

    //criação de menu para o usuário;
    public static String menuNovoPrograma(){
        String respostaUsuario = JOptionPane.showInputDialog("Deseja continuar?");
        int dadoA = 1;
        int dadoB = 1;
            if (respostaUsuario.equals("sim")){
                calcularDados(dadoA,dadoB);
            }else {
                JOptionPane.showMessageDialog(null, "SAIU");
            }
            return respostaUsuario;
    }

    //Metódo para calcular dado1 e dado2 e mostrar o menu para o usuário;
    public static void meuProgramaNovoInteiro(){
        int dadoSegundo = 1;
        int dadoPrimeiro = 1;
        calcularDados(dadoPrimeiro,dadoSegundo);
        menuNovoPrograma();
    }

    //Minha classe principal
    public static void main(String[] args){
        meuProgramaNovoInteiro();
    }
}
