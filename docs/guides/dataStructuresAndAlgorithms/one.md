---
title: 栈的封装
---

```html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>00-栈的封装</title>
  </head>
  <body>
    <script>
      function Stack() {
        this.arr = [];
        Stack.prototype.push = function (ele) {
          this.arr.push(ele);
        };
        Stack.prototype.pop = function () {
          return this.arr.pop();
        };
        Stack.prototype.peek = function () {
          return this.arr[this.arr.length - 1];
        };
        Stack.prototype.size = function () {
          return this.arr.length;
        };
        Stack.prototype.toString = function () {
          let str = "";
          for (let i = 0; i < this.arr.length; i++) {
            str += this.arr[i] + " ";
          }
          return str;
        };
      }

      let s = new Stack();
     
    </script>
  </body>
</html>

```