# CSC-331H practice Questions
//Question 2
int list<T> smaller(T item)
{ int count = 0;
  Node<T>*p = head;
  if(p!=NULL&&p->key< item){
    count++;
    p= p->next;
  }
  return count;
}
//Question 1
int clist<T> howmany(T item) //->1->2->2->4->8->first
{
   if(first=NULL)
     return 0;
   int count = 0;
  Node<T>*p = head->next;
  do{
    if(p->key==item)
    count++;
    p= p->next;
   }
  while(p!=first->next&&p->key< =item);

  return count;
}
//#Question N 8
//use assert with return val associated with te
void list<T>::getLargest(T&large)
{
  if (first!=NULL)
  {
    large = first->infos;
    Node<T> *p =first->next;
    while(p!=NULL)
    {
      if (p->infos >large)
      {
        large = p->infos;
        p = p->next;
      }

    }
  }
}
//#Question N9
void list<T>::printerGreater(T item, node<t> * p)
{
  if(p!=NULL)
  {
     if(p->infos> item)
     {
       cout<<p->info<<" ";

     }
     printerGreater(item, p->next);
  }
}

//#
int list<T> occur (T item, Node<T>* p)
 {
   if(p==NULL||p->infos =item)
   return 0;
   else if(p->infos ==item)
   {
     return 1+ occur(item, p->next);
     
   }
   else
    return occur(item, p->next);
 }
