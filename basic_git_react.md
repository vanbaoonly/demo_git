# demo_git
git init
git add . 
git commit "comment"
git remote add origin "url.git"
git push  origin master

dowload 
git clone "url"
git checkout (commit)


#Basic React
- state :  là một đối tượng chứa dữ liệu có thể thay đổi trong component. khi state thay đổi React sẽ cập nhật  giao diện hiển thị của component tương ứng , thường được sử dụng để lưu trữ các thông tin cần thiết cho component như trạng thái hiện tại, từ API ,giá trị nhập từ người dùng.
vd:
import React, { useState } from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  const increment = () => {
    setCount(count + 1);
  };
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
- provs : là các giá trị được truyền từ component cha đến component con ( có thể truyền bất kỳ dữ liệu nào như : số, chuỗi, mảng, đối tượng).
vd:
import React from 'react';
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
function App() {
  return <Greeting name="John" />;

- component : là các khối xây dựng độc lập mà bạn có thể tạo ra để tái sử dụng và quản lý giao diện người dùng
  *(có 2 loại component : Function và Class)
  Function:
function De_mo(props) {
  return <button>{props.label}</button>;

}
 Class:
 class Button extends Component {
  render() {
    return <button>{this.props.label}</button>;
  }
}
ex
