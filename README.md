# linked-list
#remove linked list element
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */
struct ListNode* removeElements(struct ListNode* head, int val) {
    struct ListNode *dummyNode=(struct ListNode*)malloc(sizeof(struct ListNode));
    dummyNode->next=head;
    struct ListNode *curr=dummyNode;
    while(curr->next){
        if(curr->next->val==val){
            curr->next=curr->next->next;
        }
        else{
            curr=curr->next;
        }
    }

    return dummyNode->next;
}
