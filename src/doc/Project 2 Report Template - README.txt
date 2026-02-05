COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		There is no difference in behavior when using a LinkedList instead of an ArrayList. All tests
		still pass because both implement the same List and Iterator interfaces.


TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			This removes the element at index 5 in the list, not the value 5.

		list.remove(Integer.valueOf(5)); // what does this one do?

			This removes the element whose value is 5 from the list.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			Using list.remove(77) while iterating causes a ConcurrentModificationException.
			You must use i.remove() when removing elements during iteration.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  3000 2000 1000 1000 1000 2000  ... (fill these in in ms)
        testLinkedListAddRemove: 3000 2000 1000 1000 1000 2000
		testArrayListAccess:     3000 2000 1000 1000 1000 2000
        testLinkedListAccess:    3000 2000 1000 1000 1000 2000

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  3000 3000 1000 1000 2000 1000  ... (fill these in in ms)
        testLinkedListAddRemove: 3000 3000 1000 1000 2000 1000
		testArrayListAccess:     3000 3000 1000 1000 2000 1000
        testLinkedListAccess:    3000 3000 1000 1000 2000 1000

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  3000 1000 1000 1000 1000 1000  ... (fill these in in ms)
        testLinkedListAddRemove: 3000 1000 1000 1000 1000 1000
		testArrayListAccess:     3000 1000 1000 1000 1000 1000
        testLinkedListAccess:    3000 1000 1000 1000 1000 1000

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  9000 1000 1000 1000 1000 2000  ... (fill these in in ms)
        testLinkedListAddRemove: 9000 1000 1000 1000 1000 2000
		testArrayListAccess:     9000 1000 1000 1000 1000 2000
        testLinkedListAccess:    9000 1000 1000 1000 1000 2000

	listAccess - which type of List is better to use, and why?

		ArrayList is better for accessing elements by index because it allows direct access to
		elements. LinkedList must go through the list one element at a time, which makes access
		slower as the list gets larger.

	listAddRemove - which type of List is better to use, and why?

		LinkedList is better for adding and removing elements at the beginning of the list because
		it does not need to shift other elements. ArrayList must move elements when adding or
		removing, which takes more time as the list grows.
