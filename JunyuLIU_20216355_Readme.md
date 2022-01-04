## Readme

### Structure of the program

The program contains one java file - Main.java, in which contains three classes. The structures of each class are presented as below, with the explanations of fields and methods.

- **Class Main( )**
  - Main operations of this program, including reading input, converting into tree, traverse tree and output the final result.
  - **Methods:**
    - **public static void main(String[] args)** - main method of the program.
    - **public static ArrayList<String> ReadInput()** - Read the user input, and sepertae the input string into an ArrayList of tokens.
    - **public static ArrayList<String> ConvertToSuffix(ArrayList<String> strInfix)** - Convert the Infix-represented ArrayList of tokens into a suffix-represented list, in oder to prepare for puting it into a tree.
    - **public static ParseTree ConvertToSuffix(ArrayList<String> LD_suffix)** - Create a tree and put the tokens in the suffix-represented list into the tree.
- **Class Node( )**
  - Used as a recursive way to create the tree, and contains methods to check for properties of the node.
  - **Fields:** 
    - **String literal** - String value of the node.
    - **Node leftChild** - A reference to its left child node (which node to point to).
    - **Node rightChild** - A reference to its right child node (which node to point to).
  - **Methods:** 
    - **Node(String literal)** - The constructor of the Node class.
    - **setLeftNode(Node leftChild)** - Set the value (which node to point to) of the left child of the current node.
    - **setRightNode(Node rightChild)** - Set the value (which node to point to) of the right child of the current node.
    - **boolean isLeaf( )** - Check whether the current node is a leaf node.
    - **boolean isEqual( )** - Check whether the left branch of the current node equals to its right branch.
- **Class ParseTree( )**
  - Used as the structure of the tree, and contains methods to traverse, change and merge the tree.
  - **Fields:**
    - **Node root** - The root node of the tree.
    - **private static int numTransferable** - The number of transferable nodes (e.g. containing a node with literal "->") in the tree.
  - **Methods:** 
    - **public static void traverseTree(Node node)** - Traverse through the tree following preorder traversal, and change the traversed node if its traversable.
    - **public static int traverseTreeCheck(Node node)** - Traverse through the tree following preorder traversal and return the numebr of transferable nodes.
    - **public void resetNumTransferable( )** - reset numTransferable to 0.
    - **public static boolean checkTransform(Node node)** - Check whether the current node is transferable (satisfy the transfer rules). 
    - **public static boolean doTransform(Node node)** - Change the traversed node if its traversable.
    - **public static String printMe(Node node)** - Traverse through the tree following preorder traversal and merge the literals of all the nodes into a single string, as the final output.

### How to Run the Program

Open the "JunyuLIU_20216355_Code" folder in IntelliJ IDEA, setting the SDK as version 15 and could run it.

