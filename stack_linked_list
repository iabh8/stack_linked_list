#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node *next;
};

struct node *head;

void push(int data){
    struct node *ptr;
    ptr = (struct node *)malloc(sizeof(struct node));
    
    if (ptr == NULL){
        printf("\nCouldn't push");
    }
    else{
        if (head == NULL){
            ptr->data = data;
            ptr->next = NULL;
            head = ptr;
        }
        else{
            ptr->data = data;
            ptr->next = head;
            head = ptr;
        }
        printf("\nNode pushed!");
    }
}

void display(){
    struct node *current;
    current = (struct node *)malloc(sizeof(struct node));
    
    if (head == NULL){
        printf("\nUnderflow");
    }
    else{
        printf("\n");
        current = head;
        while (current!=NULL){
            printf("%d\t",current->data);
            current = current->next;
        }
    }
}

void pop(){
    struct node *ptr;
    ptr = (struct node *)malloc(sizeof(struct node));
    
    if (head == NULL){
        printf("\nUnderflow");
    }
    else{
        ptr = head;
        head = head->next;
        printf("\n%d deleted!",ptr->data);
        free(ptr);
    }
}

void main(){
    push(10);
    push(20);
    push(30);
    display();
    pop();
    display();
}
