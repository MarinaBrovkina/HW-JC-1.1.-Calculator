public class Main {

    public static void main(String[] args) {
        Calculator calc = Calculator.instance.get();
        int a = calc.plus.apply(1, 2);
        int b = calc.minus.apply(1, 1);
        int c = calc.devide.apply(a, b);
        int d = calc.abs.apply(-1);
        try {
            calc.println.accept(c);
        } catch (ArithmeticException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
//Ошибка возникает из-за деления на ноль, если исправить в стр.6 размер переменной, чтобы итоговый результат был <0, то код срабатывает