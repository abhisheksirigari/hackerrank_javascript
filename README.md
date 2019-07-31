## Moonsoon Umberallas
```javascript
const biggerUmbrella = Math.max(...p)
    const remain = n % biggerUmbrella
    const peopleThatFit = Math.floor(n / biggerUmbrella)

    if (remain >= 1 && p.length === 1) {
        return -1
    } else {
        const remainingUmbrellas = p.filter(umbrella => umbrella !== biggerUmbrella)
        return remain !== 0 ? solve(remain, remainingUmbrellas) + peopleThatFit : peopleThatFit
    }
```
## Binary number in a linked list
```javascript
function getNumber(binary) {
    // Write your code here
      function Node (data, next) 
  {  
      this.data = data;  
      this.next = next;  
  }  
  
  // Returns decimal value of binary linked list / 
   function decimalValue(head)  
  {  
      // Initialized result  
      let res = 0;  
    
      // Traverse linked list  
      while (head != null)  
      {  
          // Multiply result by 2 and add  
          // head's data  
          res = (res << 1) + (head.data?1:0);  
    
          // Move next  
          head = head.next;  
      }  
      return res;  
  }  
  
  // Utility function to create a new node.  
   function newNode(data)  
  {  
      let temp = new Node(data==1? true:false, null);  
      return temp;  
  }

  return decimalValue(binary);   
 

}
```
