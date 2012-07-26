8.
==

11)  Write code to remove duplicates from an unsorted linked list.
FOLLOW UP
How would you solve this problem if a temporary buffer is not allowed?


This is the simple way where two loops are used. Outer loop is used to pick the elements one by one and inner loop compares the picked element with rest of the elements. (If no additional buffers are not allowed )

If additional buffers are allowed then will use HashSet. We traverse the link list from head to end. For every newly encountered element, we check whether it is in the hash table: if yes, we remove it; otherwise we put it in the hash table.

import java.util.LinkedList;

public class CheckingDuplication {
  static int temp;

	public static void main(String[] args) {
		LinkedList<Integer> l1 = new LinkedList<Integer>();
		l1.add(21);
		l1.add(14);
		l1.add(11);
		l1.add(25);
		l1.add(6);
		l1.add(1);
		l1.add(3);
		l1.add(4);
		l1.add(99);

		System.out.println(l1.size());
		// System.out.println(l1.get(0));
		// System.out.println(l1.get(1));
		// System.out.println(l1.get(8));

		for (int i = 0; i < l1.size(); i++) {
			for (int j = i+1; j < l1.size(); j++) {
				if (l1.get(i) == l1.get(j)) {
			System.out.println("temp " + l1.get(i) + " get(j) "+ l1.get(j));
							
			System.out.println("Linked list contains duplicate");
					System.exit(1);
				}
			}
			
		}
		System.out.println("There r no duplicates in Linked List");
	}
}
