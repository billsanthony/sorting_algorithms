 

AIM 🌻
At least four different sorting algorithms
What is the Big O notation, and how to evaluate the time complexity of an algorithm
How to select the best sorting algorithm for a given input
What is a stable sorting algorithm
Tests ✔️
tests: Folder of test files.
Helper Files 🙌
print_array.c: C function that prints an array of integers.
print_list.c: C function that prints a listint_t doubly-linked list.
Header Files 📁
sort.h: Header file containing definitions and prototypes for all types and functions written for the project.
Data Structure and Functions For this project you are given the following print_array, and print_list functions: #include <stdlib.h> #include <stdio.h>

/**

print_array - Prints an array of integers

@array: The array to be printed

@size: Number of elements in @array */ void print_array(const int *array, size_t size) { size_t i;

i = 0; while (array && i < size) { if (i > 0) printf(", "); printf("%d", array[i]); ++i; } printf("\n"); } #include <stdio.h> #include "sort.h"

/**

print_list - Prints a list of integers

@list: The list to be printed */ void print_list(const listint_t *list) { int i;

i = 0; while (list) { if (i > 0) printf(", "); printf("%d", list->n); ++i; list = list->next; } printf("\n"); } Our files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction. Please declare the prototype of the functions print_array and print_list in your sort.h header file Please use the following data structure for doubly linked list: /**

struct listint_s - Doubly linked list node

@n: Integer stored in the node

@prev: Pointer to the previous element of the list

@next: Pointer to the next element of the list */ typedef struct listint_s { const int n; struct listint_s *prev; struct listint_s *next; } listint_t; Please, note this format is used for Quiz and Task questions.

O(1) O(n) O(n!) n square -> O(n^2) log(n) -> O(log(n)) n * log(n) -> O(nlog(n)) n + k -> O(n+k) … Please use the “short” notation (don’t use constants). Example: O(nk) or O(wn) should be written O(n). If an answer is required within a file, all your answers files must have a newline at the end.

Tests Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org ![] (https://www.random.org/integer-sets/)

Data Structure:

typedef struct listint_s
{
	const int n;
	struct listint_s *prev;
	struct listint_s *next;
} listint_t;
Function Prototypes:

File	Prototype
print_array.c	void print_array(const int *array, size_t size)
print_list.c	void print_list(const listint_t *list)
0-bubble_sort.c	void bubble_sort(int *array, size_t size);
1-insertion_sort_list.c	void insertion_sort_list(listint_t **list);
2-selection-sort.c	void selection_sort(int *array, size_t size);
3-quick_sort.c	void quick_sort(int *array, size_t size);
100-shell_sort.c	void shell_sort(int *array, size_t size);
101-cocktail_sort_list.c	void cocktail_sort_list(listint_t **list);
102-counting_sort.c	void counting_sort(int *array, size_t size);
103-merge_sort.c	void merge_sort(int *array, size_t size);
104-heap_sort.c	void heap_sort(int *array, size_t size);
105-radix_sort.c	void radix_sort(int *array, size_t size);
106-bitonic_sort.c	void bitonic_sort(int *array, size_t size);
107-quick_sort_hoare.c	void quick_sort_hoare(int *array, size_t size);
deck.h: Header file containing definitions and prototypes for all types and functions written for the task 1000-sort_deck.c.
Data Structures:

typedef enum kind_e
{
	SPADE = 0,
	HEART,
	CLUB,
	DIAMOND
} kind_t;
typedef struct card_s
{
	const char *value;
	const kind_t kind;
} card_t;
typedef struct deck_node_s
{
	const card_t *card;
	struct deck_node_s *prev;
	struct deck_node_s *next;
} deck_node_t;
Function Prototype:

File	Prototype
1000-deck_node.c	void sort_deck(deck_node_t **deck);
