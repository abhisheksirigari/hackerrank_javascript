## Moonsoon Umberallas Javascript
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
## Binary number in a linked list Javascript
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


## prefixtopostfix Javascript 
```javascript
function preToPost(prefixes) {
    // funtion to check if character
    // is operator or not
    function isOperator(x) {
      switch (x) {
        case '+':
        case '-':
        case '/':
        case '*':
          return true;
      }
      return false;
    }
    
    // let pre_fix = prefixes.toString();
    let pre_fix = prefixes;

    let output = [];
    let input = pre_exp.split('');

    // length of expression
    const length = pre_exp.length;

    // reading from right to left
    for (let i = length - 1; i >= 0; i--) {
      // check if symbol is operator
      if (isOperator(pre_exp.charAt(i))) {
        // pop two operands from stack
        const op1 = output.pop();
        const op2 = output.pop();

        // concat the operands and operator
        const temp = op1 + op2 + pre_exp.charAt(i);

        // Push String temp back to stack
        output.push(temp);
      }

      // if symbol is an operand
      else {
        // push the operand to the stack
        output.push(pre_exp.charAt(i) + '');
      }
    }

    // stack contains only the Postfix expression
    return output.join('');
  }

```
