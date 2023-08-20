### What happened if 2 pointers are substracted from each other?
This operation means -> how many values ,of the same type of the 2 pointers, are there ?


```c
#include <stdio.h>
int main() {
  
 int *ptr1, *ptr2;

  ptr1 = 100;
  ptr2 = 200;
   printf(" to know how many integers can be stored between ptr2 and ptr1 -> ptr2 - ptr1 = %i", ptr2 - ptr1); // ((200 - 100)/sizeof(int )
 
  return 0;
}
```
![image](https://github.com/toqaezzatly/C_SelfStudying/assets/104696786/c6a95bd4-908b-4459-be57-6f4e6747390e)
```
 to know how many integers can be stored between ptr2 and ptr1 -> ptr2 - ptr1 = 25 to know how many integers can be stored between ptr2 and ptr1 -> ptr2 - ptr1 = 25
```
## adding 2 pointers is not valid, since it is meaningless
------------------------------------------------------------------
### If all pointer have the same size in memory,  why we don't just pin **void** why other data types in pointers ?
pointers data type are important to determine the access and step size.
```c
#include <stdio.h>
int main() {
  unsigned char *p;
  char *c;
  unsigned char x = 255;
  
  p = &x;
  c = &x;
  printf("*p = %i \n*c = %i", *p, *c);
  return 0;
}
```
![image](https://github.com/toqaezzatly/C_SelfStudying/assets/104696786/1d579098-e92b-44e6-a703-ecfc6f01d3ef) ![image](https://github.com/toqaezzatly/C_SelfStudying/assets/104696786/796bc2f4-91db-4a53-b76e-a9eb361a7c50)


### Casting with pointer 
**why?**
It differs only in access but not in step 
```c
#include <stdio.h>
int main() {
  
  unsigned short x = 1026;
  unsigned short *ptr = &x;
  
  printf("As a short : %i\n", *ptr);
  // In the next line it will access only the first
  // Byte instead of 2
  printf("AS a char : %i", *(unsigned char* )ptr);
 
  return 0;
}
```
![image](https://github.com/toqaezzatly/C_SelfStudying/assets/104696786/38c14c60-b66c-448d-8355-be215c2c3629)

