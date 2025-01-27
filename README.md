/*
Arrays and Array Lists are both used to store multiple items in one variable. The differences are rather straight forward.  Here are most of the differences:
Arrays:
•	Fixed size - You can't change the size once it's created.
•	Can store both primitive data types (like int, char) and objects.
•	Fast access to elements by their index.

Array Lists:
•	Resizable - You can add or remove elements anytime.
•	Can only store objects (but can use autoboxing to store primitives).
•	Easier to add, remove, and change elements.


In essence there are a few key areas that make arrays and array lists different.  One area of difference is size. Arrays are fixed in size, while Array Lists can grow and shrink.  
Additionally, we see different characteristics around flexibility.  Array Lists are more flexible with built-in methods for easy list manipulation.  An additional difference can be seen in Type Storage.  
Arrays can hold both primitive types and objects. Array Lists can only hold objects.
*/

package differencearraysarraylists;

import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Array example: Storing Hobie Cat model lengths
        int[] hobieCatLengths = new int[5];
        hobieCatLengths[0] = 16;
        hobieCatLengths[1] = 14;
        hobieCatLengths[2] = 18;
        hobieCatLengths[3] = 21;
        hobieCatLengths[4] = 17;

        System.out.println("Hobie Cat model lengths (Array):");
        for (int i = 0; i < hobieCatLengths.length; i++) {
            System.out.println(hobieCatLengths[i] + " feet");
        }

        // ArrayList example: Storing Hobie Cat names
        ArrayList<String> hobieCatNames = new ArrayList<>();
        hobieCatNames.add("Hobie 16");
        hobieCatNames.add("Hobie 14");
        hobieCatNames.add("Hobie 18");
        hobieCatNames.add("Hobie Mirage Tandem Island");
        hobieCatNames.add("Hobie Getaway");

        System.out.println("\nHobie Cat model names (ArrayList):");
        for (int i = 0; i < hobieCatNames.size(); i++) {
            System.out.println(hobieCatNames.get(i));
        }

        // Differences demonstration
        hobieCatNames.add("Hobie Bravo"); // Adding a new Hobie Cat model
        System.out.println("\nHobie Cat models after adding a new one (ArrayList):");
        for (int i = 0; i < hobieCatNames.size(); i++) {
            System.out.println(hobieCatNames.get(i));
        }

        // Arrays can't be resized. The following line would cause an error:
        // hobieCatLengths[5] = 19;
    }
}
