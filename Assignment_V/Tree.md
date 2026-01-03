# Section A. Understand and clearly define:

**1. General Tree**  

A **General Tree** is a non-linear data structure consisting of nodes organized in a hierarchical manner.Each node can have zero or multiple child nodes. There is **no limit** on the number of children a node can possess.

**2. Binary Tree**  

A **Binary Tree** is a tree structure where each node is restricted to having **at most two children**.

**3. Complete Binary Tree**  

A **Complete Binary Tree** is a binary tree in which every level, except possibly the last, is completely filled. On the last level, all nodes are filled from **left to right** without any gaps.

**4. Binary Search Tree (BST)**  

A **Binary Search Tree (BST)** is a binary tree that The values in its **left** subtree are strictly **less than** the node's value, and the values in its **right** subtree are strictly **greater than** the node's value.

**5. AVL Tree**  

An **AVL Tree** is a **self-balancing** Binary Search Tree (BST). It maintains a balance property where the difference in heights between the left and right subtrees of any node. If violates this property, the tree automatically performs rotations to restore balance.

**6. Red-Black Tree**  

A **Red-Black Tree** is a self-balancing BST that uses a color attribute (red or black) for each node to ensure balance. It guarantees that the longest path from the root to a leaf is no more than twice as long as the shortest path.

**7. Max Heap**  

A **Max Heap** is a complete binary tree that satisfies the heap property: the value of every parent node is **greater than or equal to** the values of its children. The largest element in the tree is always located at the root.

**8. Min Heap**  

A **Min Heap** is a complete binary tree that satisfies the heap property: the value of every parent node is **less than or equal to** the values of its children. The smallest element in the tree is always located at the root.

# Section B. Build a hierarchy and transformation path from the general tree to these variants

## 1. Tree Family Hierarchy Diagram
This diagram illustrates the specialization path from the most general structure to specific variants.

```mermaid
graph TD
    GT[General Tree] -->|Limit children to 2| BT[Binary Tree]
    BT -->|Fill level-by-level| CBT[Complete Binary Tree]
    BT -->|Sort: Left < Root < Right| BST[Binary Search Tree]
    BT -->|Heap Property: Parent >= Child| MaxH[Max Heap]
    BT -->|Heap Property: Parent <= Child| MinH[Min Heap]
    
    BST -->|Balance Height <= 1| AVL[AVL Tree]
    BST -->|Color Rules & Balance| RB[Red-Black Tree]
```



| From | To | New Property / Constraint Added |
| :--- | :--- | :--- |
| **General Tree** | **Binary Tree** | Limit children to 2 |
| **Binary Tree** | **Complete Binary Tree** | Fill level-by-level |
| **Binary Tree** | **Binary Search Tree (BST)** | Sort: Left < Root < Right |
| **BST** | **AVL Tree** | Balance Height <= 1 |
| **BST** | **Red-Black Tree** | Color Rules & Balance |
| **Binary Tree** | **Max Heap** | Heap Property: Parent >= Child |
| **Binary Tree** | **Min Heap** | Heap Property: Parent <= Child |

# Section C. Tree Constructions Using Given Integers

**Given Integers:**
`37, 142, 5, 89, 63, 117, 24, 176, 58, 133, 92, 11, 151, 72, 39, 184, 7, 101, 54, 160`

---

#### 1. Binary Tree
* **Tool name / URL**: [e.g., treeconverter](https://treeconverter.com/)
* **Construction description**: Inserted the integers in the given order. Since no specific balancing or sorting rule is required for a general binary tree, I placed nodes using a level-order strategy (filling top to bottom, left to right) to maintain a structural form similar to a complete binary tree.
* **Screenshot**:
    > ![Binary Tree Screenshot](<img width="1520" height="542" alt="image" src="https://github.com/user-attachments/assets/95ab5f06-3552-4e80-847c-047e43f52c1a" />)

#### 2. Complete Binary Tree
* **Tool name / URL**: [e.g., Draw.io or USFCA Tool]
* **Construction description**: Constructed by filling nodes strictly from top to bottom and left to right. No gaps were left. The root is 37, the left child is 142, the right child is 5, and so on.
* **Screenshot**:
    > ![Complete Binary Tree Screenshot](place_your_image_link_here.png)

#### 3. Binary Search Tree (BST)
* **Tool name / URL**: [e.g., USFCA BST Visualizer]
* **Construction description**: Inserted elements sequentially. For each value, I compared it with the root: smaller values went to the left subtree, and larger values went to the right subtree. No balancing operations were performed.
* **Screenshot**:
    > ![BST Screenshot](place_your_image_link_here.png)

#### 4. AVL Tree
* **Tool name / URL**: [e.g., USFCA AVL Tree Visualizer]
* **Construction description**: Inserted elements sequentially. After every insertion, the tree checked the balance factor of each node. If any node's balance factor became other than -1, 0, or 1, appropriate rotations (LL, RR, LR, or RL) were performed to restore balance.
* **Screenshot**:
    > ![AVL Tree Screenshot](place_your_image_link_here.png)

#### 5. Red-Black Tree
* **Tool name / URL**: [e.g., USFCA Red-Black Tree Visualizer]
* **Construction description**: Inserted elements using standard BST insertion, initially coloring new nodes red. Then, fixed any violations of Red-Black properties (such as double red nodes) using recoloring and rotations.
* **Screenshot**:
    > ![Red-Black Tree Screenshot](place_your_image_link_here.png)

#### 6. Max Heap
* **Tool name / URL**: [e.g., USFCA Heap Visualizer]
* **Construction description**: Built using the insertion method. Each new element was added to the next available position in the complete binary tree structure and then "bubbled up" (swapped with its parent) until the heap property (Parent ≥ Child) was satisfied.
* **Screenshot**:
    > ![Max Heap Screenshot](place_your_image_link_here.png)

#### 7. Min Heap
* **Tool name / URL**: [e.g., USFCA Heap Visualizer]
* **Construction description**: Similar to the Max Heap, but enforced the property that Parent ≤ Child. New elements were inserted at the end and bubbled up if they were smaller than their parent.
* **Screenshot**:
    > ![Min Heap Screenshot](place_your_image_link_here.png)
