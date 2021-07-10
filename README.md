# Tower-Of-Hanoi
Program of tower of hanoi using Java


public class Main
{
    static void towerOfHanoi(int n, char source, char destination, char helper){
        if(n == 1){
            System.out.println("move disk 1 from rod "+source+ " to rod "+destination);
            return;
        }
        towerOfHanoi(n-1, source, helper, destination);
        System.out.println("move disk "+n+ " from rod "+source+ " to rod "+destination);
        towerOfHanoi(n-1, helper, destination, source);
    }
	public static void main(String[] args) {
		int n = 4;
		towerOfHanoi(n, 'A', 'C', 'B');
	}
}

OUTPUT:
move disk 1 from rod A to rod B
move disk 2 from rod A to rod C
move disk 1 from rod B to rod C
move disk 3 from rod A to rod B
move disk 1 from rod C to rod A
move disk 2 from rod C to rod B
move disk 1 from rod A to rod B
move disk 4 from rod A to rod C
move disk 1 from rod B to rod C
move disk 2 from rod B to rod A
move disk 1 from rod C to rod A
move disk 3 from rod B to rod C
move disk 1 from rod A to rod B
move disk 2 from rod A to rod C
move disk 1 from rod B to rod C
