
Basic operation
0. Initial
1. Insert x after t
2. remove x after t
3. traverse list
4. IsEmpty


List Type
a. circular
  0.  head->next = head;
  1.  x->next = t->next; t->next = x;
  2.  t->next = x->next
  3.  t= head;
      do{...; t=head->next;}while(t!=head);
  4.  (head->next == head)
b. Head pointer, null tail
  0.  head = new node();
  1.  x->next = t->next; t->next = x;
  2.  t->next = x->next;
  3.  for(t = head;t!=NULL; t=t->next){...}
  4.  (head->next== NULL)

c. Dummy head node, null tail
  0.  head = node(); head->next = NULL;
  1.  x->next = t->next; t->next = x;
  2.  t->next = x->next;
  3.  for(t=head->next; t != NULL; t= t->next){}
  4.  (head->next == NULL)
  
d. Dummy head node(always 1 real object, last node points first object)
  0.  head = new node(); head->next = p; p->next = p
  1.  x->next = t->next; t->next = x;
  2.  t->next = x->next;
  3.  for(t=head->next; t!=p; t= t->next)
  4. (head->next = p)
  
