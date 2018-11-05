# CS2302-Lab3
This is lab 3 almost complete
from BST_Node import BinarySearchTree
from BST_Node import Node
from Avl_TreeNode import AvlNode
from Avl_TreeNode import AVLTree
from RBTNode import RedBlackTree

def read_file():
    we = open('glove.6B.50d.txt')
    word_embedding = we.readlines()

    word_tree = BinarySearchTree()
    avl_tree = AVLTree()
    rb_tree = RedBlackTree

    word = word_embedding
    tree = input("What tree do you want to use?")
    print(tree)
    print(" This is the BST implementation")

    for i in word:
        words = Node(word_embedding)
        tree.insert(words)
        print(word_tree[i])

    if tree is "AVL":
        for j in word:
            avl_word =  AvlNode(word)
            avl_tree.avl_insert(avl_word)
            print(avl_tree[j])

    if tree is "Red-Black":
        rb_root = word.rb_insert
        for w in word:
            rb_word = rb_tree.rb_insert_node()
            print(rb_root)
            print(rb_word[w])
        we.close()


def count_nodes(root):
    sum_node = 0
    while root is not None:
        sum_node = 1 + count_nodes(root.right) + count_nodes(root.left)
     print(sum_node)


def dot_product(vector1, vector2):
    sum1 = vector1
    sum2 = vector2

    product = sum1 + sum2
    return product

def magnitude(vector1, vector2):
    sum1 = vector1 **2
    sum2 = vector2 **2

    mag = (sum1 + sum2) ** (1/2)
    return mag

def similarity(e0, e1):
    n_product = e0 * e1
    d_product = abs(e0) *abs(e1)
    f_product = n_product/d_product
    return f_product

def find_height(root):
    count1 = 0
    count2 = 0
    if root.right is not None:
        count1 = 1 + find_height(root.right)
    if root.left is not None:
        count2 = 1 + find_height(root.left)

    if count1 > count2:
        return count1
    else:
        return count2

def create_file()
    kw= open("ordered_words.txt","w+")
    for i in range(word_embedding.length):
        print (word_embedding[i])


read_file()
