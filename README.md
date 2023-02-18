câu 1
import java.util.Scanner;

public class PhuongTrinhBacNhat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a, b;
        System.out.print("Nhap he so a: ");
        a = sc.nextDouble();
        System.out.print("Nhap he so b: ");
        b = sc.nextDouble();

        if (a == 0) {
            if (b == 0) {
                System.out.println("Phuong trinh co vo so nghiem");
            } else {
                System.out.println("Phuong trinh vo nghiem");
            }
        } else {
            double x = -b / a;
            System.out.println("Phuong trinh co nghiem x = " + x);
        }
    }
}
câu 2
import java.util.Scanner;

public class PhuongTrinhBacHai {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a, b, c;
        System.out.print("Nhap he so a: ");
        a = sc.nextDouble();
        System.out.print("Nhap he so b: ");
        b = sc.nextDouble();
        System.out.print("Nhap he so c: ");
        c = sc.nextDouble();

        if (a == 0) {
            System.out.println("Day la phuong trinh bac nhat");
            if (b == 0) {
                if (c == 0) {
                    System.out.println("Phuong trinh vo so nghiem");
                } else {
                    System.out.println("Phuong trinh vo nghiem");
                }
            } else {
                double x = -c / b;
                System.out.println("Phuong trinh co nghiem x = " + x);
            }
        } else {
            double delta = b * b - 4 * a * c;
            if (delta < 0) {
                System.out.println("Phuong trinh vo nghiem");
            } else if (delta == 0) {
                double x = -b / (2 * a);
                System.out.println("Phuong trinh co nghiem kep x = " + x);
            } else {
                double x1 = (-b + Math.sqrt(delta)) / (2 * a);
                double x2 = (-b - Math.sqrt(delta)) / (2 * a);
                System.out.println("Phuong trinh co 2 nghiem phan biet:");
                System.out.println("x1 = " + x1);
                System.out.println("x2 = " + x2);
            }
        }
    }
}
câu 3
import java.util.Scanner;

public class TinhTienDien {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhập số điện sử dụng trong tháng: ");
        int soDien = sc.nextInt();

        int tien;
        if (soDien <= 50) {
            tien = soDien * 1000;
        } else {
            tien = 50 * 1000 + (soDien - 50) * 1200;
        }

        System.out.println("Số tiền điện phải trả: " + tien + " VNĐ");
    }

}
câu 4 
import java.util.Scanner;

public class Menu {

    public static void main(String[] args) {
        int chucNang;
        Scanner sc = new Scanner(System.in);

        do {
            menu();
            System.out.print("Chọn chức năng: ");
            chucNang = sc.nextInt();

            switch (chucNang) {
                case 1:
                    giaiPTB1();
                    break;
                case 2:
                    giaiPTB2();
                    break;
                case 3:
                    tinhTienDien();
                    break;
                case 4:
                    System.out.println("Kết thúc chương trình");
                    break;
                default:
                    System.out.println("Chức năng không hợp lệ. Vui lòng chọn lại!");
                    break;
            }
        } while (chucNang != 4);
    }

    public static void menu() {
        System.out.println("+---------------------------------------------------+");
        System.out.println("1. Giải phương trình bậc nhất");
        System.out.println("2. Giải phương trình bậc 2");
        System.out.println("3. Tính tiền điện");
        System.out.println("4. Kết thúc");
        System.out.println("+---------------------------------------------------+");
    }

    public static void giaiPTB1() {
        // Chứa mã của bài giải phương trình bậc nhất
        System.out.println("Bạn chọn chức năng giải phương trình bậc nhất");
    }

    public static void giaiPTB2() {
        // Chứa mã của bài giải phương trình bậc hai
        System.out.println("Bạn chọn chức năng giải phương trình bậc hai");
    }

    public static void tinhTienDien() {
        // Chứa mã của bài tính tiền điện
        System.out.println("Bạn chọn chức năng tính tiền điện");
    }

}
