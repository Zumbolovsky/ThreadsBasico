public class Pai {

    protected int[] numeros = new int[] {1, 2, 3};
    
    public static void main(String[] args) throws InterruptedException {
        System.out.println("Agora vamos compartilhar essa memoria");
        
        Thread f1 = new Filho(0, "Primogenito");
        Thread f2 = new Filho(1, "Do Meio");
        Thread f3 = new Filho(2, "Cacula");
        
        System.out.println("Vamos comecar:");
        
        f1.start();
        f2.start();
        f3.start();
        
        f1.join();
        f2.join();
        f3.join();
        
        System.out.println("Kbo");
    }
    
}
