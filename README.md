# Fundamentos
package fundamentos;

/* Variables o metodos de clases son static
// Variables o metodos de instancia no son static
// Para accede a un metodo o varibles static es:
// NombreClase.Metodo o NombreClase.Variable
*/

// Universidad de guayaquil 
// L.S.I (3er semestre)


class CuentaBancaria{
    public int saldo;
    public static int numero=0;
}
    public class variables {
        public static void sumarSaldo(CuentaBancaria cta){
            cta.saldo +=50;
        }
        
        public static void sumarSaldo(int saldo){
            saldo +=30;
        }
    //............crear minimo 10 objetos CuentaBancaria y probar, probar, y probar...............//
        
    public static void main(String[] args) {
      //1)Y 2)
      
        CuentaBancaria ctA=new CuentaBancaria();
        
        CuentaBancaria ctB=ctA;
        
        ctA.saldo=1000;
        sumarSaldo(ctA);
        sumarSaldo(ctB);
        
        System.out.println("ctA:" +ctA.saldo);// Imprime 1100 //
        System.out.println("ctB:" +ctB.saldo);// Imprime 1100 //
        
        // 3)
        
        ctB.saldo=250;
        CuentaBancaria ctC = ctB;
        sumarSaldo(ctC);
        System.out.println("ctC:" +ctC.saldo);// imprime 300 //
        
        // 4)
        
        ctC.saldo=1280;
        CuentaBancaria ctD = ctC;
        sumarSaldo (ctD);
        System.out.println("ctD:" +ctD.saldo); // imprime 1330 //
        
        // 5)
        
        CuentaBancaria ctE = ctD;
        sumarSaldo (ctE);
        System.out.println("ctE:" +ctE.saldo);// imprime 1380 //
        
        // 6)
        
        CuentaBancaria ctF = new CuentaBancaria();
        ctF.saldo=120;
        
        // 7)
        CuentaBancaria ctG = ctB;
        ctG.saldo=1220;
        sumarSaldo (ctF);
        sumarSaldo (ctG);
        System.out.println("ctF:" +ctF.saldo);// imprime 170 //
        System.out.println("ctG:"+ctG.saldo);// imprime 1270 //
        
        // 8)
        
        CuentaBancaria ctH = ctC;
        sumarSaldo (ctH);
        
        // 9)
        
        CuentaBancaria ctI = ctF;
        sumarSaldo (ctI);
        
        // 10)
        
        CuentaBancaria ctJ = new CuentaBancaria();
        ctJ.saldo=1200;
        sumarSaldo (1000);
        System.out.println("ctH:" +ctH.saldo); // imprime 1320 //
        System.out.println("ctI:" +ctI.saldo); // imprime  220 //
        System.out.println ("EL SALDO TOTAL DE SU CUENTA ES :.......");
        System.out.println("ctJ:" +ctJ.saldo); // imprime 1200 //
       
        // FIN DEL EJERCICIO//
    }
  
}
       
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
