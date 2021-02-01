
# Module2-reflection-ngày 1/2
***
<h3> Abstrack Class là gì: </h3><br>
   -  Lớp trừu tượng được xem như 1 class cha cha tất cả các class nó cùng bản chất, và phải dùng từ khóa <strong>extends<strong><br>
   -  Không cho phép có các  tham số chỉ khai báo các thuộc tính và phương thức bình thường.<br>
   -  Các phương thức định nghĩa abstract trong abstract class chỉ khai báo tên hàm và không viết nội dung hàm đó. Nội dung sẽ đươc viết trong class kế thừa khi override lại phương thức đó
    <h3> Ví dụ </h3>
    <?php <br>
      abstract class Animal{<br>
      public $name;<br>
      abstract function run();<br>
   }<br>
      class Dog extends Animal{<br>
   } <br>
      public function run(){<br>
      echo "Con chó chạy nhanh";<br>
    }<br>
<h3> Interface là gì : </h3></br>
    -  Không phải là một lớp. Nó được mô tả như một bản thiết kế cho các class có chung cách thức hoạt động. <br>
    -  Không phải một lớp lên nó không định nghĩa thuộc tính và khởi taọ đối tượng mà chỉ khai báo phương thức <br>
    -  Các phương thức chỉ khai báo tên hàm và không viết nội dung hàm trong đó.
    -  Không có khái niệm phạm vi phương thức, tất cả là public
    -  Lớp con kế thừa interface sẽ phải ghi đè tất cả phương thức trên đó
    -  Có thể kế thừa nhiều interface khác nhau bằng từ khóa implements.
 h3> ví dụ: </h3>
      <?php
      interface Move 
   {
       function run();
   }
      class Dog implements Move
   {
       public function run () 
        echo "Con chó chạy nhanh";
    }

<h3> Khi nào dùng interface và khi nào dùng abstract Class. </h3>
   -  Nhìn chung cả 2 đều được coi như là một bản thiết kế cho các class con kế thừa nó
      - Abstract class là bản thiết kế cho class: 
         - Về bản chất abstract class là một bản class khai báo thêm các thuộc tính và phương thức khác không phải trừu tượng.
         nó được xem như bản thiết kế cho class vì những class extends lại từ nó ngoài override lại các phương thức trừu tượng 
         của nó thì có thể sử dụng nó.
         - Abstract thường được sử dụng trong trường hợp class kế thừa từ nó cùng bản chất
    
      - Interface là "bản thiết kế" cho Method:
         - Vì những class implements đều ghi đều phải override lại phương thức của nó
         - Interface thường được sử dụng trong trường hợp các kế  thừa không có cùng bản chất nh
         
      
   


      

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Module2-reflection-ngày 29/1
***
- Vòng đời của một đối tượng : 
   + Khởi tạo đối tượng: __construct() --> sử dụng đối tương --> Hủy đối tương __destruct()
   
VD:
  function __construct(){     
     echo 'Calling constructor';<br/>
  }<br/>
  function some_method(){     
      echo 'Calling a method';<br/>  
  }  
  function __destruct()    {     
       echo 'Calling destructor';<br/>   
  }<br/>
 }<br/>
 $myObject = new MyClass();<br/>
 $myObject->some_method();
   
   
- Kế thừa (Inheritance) là cơ chế cho phép một lớp con sử dụng lại các đặc điểm và hành vi của lớp cha
- Một số dạng kế thừa : 
   + Single: Một lớp kế thừa chỉ 1 lớp cha
   + Multilevel: Một lớp kế thừa tù lớp cha, lớp cha lại kế thừa lớp khác trên nó
   + Hierarchical: 1 lớp cha có nhiều lớp con với level khác nhau.
   + Multippe: Đa kế thừa -> 1 lớp con kế nhiều lớp cha (Trong JAVA không cho phép đa kế thừa )
   
- Cú pháp: 
   + class SubClass extends SuperClass{};
   trong đó: - từ khóa extends được sử dụng để kế thừa 1 lớp.
             - SubClass là tên lớp con.
             - SuperClass là tên lớp cha.
             
 - Ghi đè phương thức(Method overriding) cho phép lớp con định nghĩa lại phương thức đã định nghĩa trước đó  của lớp cha.
 
 - Từ khóa parent sử dụng trong một lớp con truy xuất các thuộc tính và phương thức của lớp cha.
 
 - Từ khóa Final hạn chế tối đa việc ghi đè, ngăn chặn kế thừa từ một lớp và việc ghi đè phương thức

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 28/1
***
- JSON là đọc dữ liệu từ máy chủ Web và hiển thị dữ liệu trong một trang web
- Chuyển đổi đối tượng PHP thành JSON ta dùng hàm json_encode(). <br/>
VD: 
<?php
$myObj->name = "tu";<br/>
$myObj->age = 30;<br/>
$myObj->city = "Ha Noi";<br/>
$myJSON = json_encode($myObj);<br/>
echo $myJSON;<br/>
?>

- Namespace là một hình thức đóng gói các hạng mục liên quan với nhau, nhóm các 
lớp, các hàm, các hàng, interface có liên quan đến nhau vào cùng một nơi.
- Cú pháp khai báo : namespace Name;
- Khi 1 class được định danh bằng 1 namespace thì sẽ có cú pháp sau:
new tenNamespace\tenClass();
VD: 
<?php
namespace my\name;

class MyClass {}
function myfunction() {}
const MYCONST = 1;
$a = new MyClass;
$c = new \my\name\MyClass;
$a = strlen('hi');
$d = namespace\MYCONST;
$d = __NAMESPACE__ . '\MYCONST';
echo constant($d);
?>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 27/1
***
- OOP mô phỏng đối tượng thực vào trong thế giới lập trình
- Khai báo một lớp bằng từ khóa class và khởi tại đối tượng bằng từ new
- Truy xuất đến thành phần đối tượng qua biến trỏ đến đối tượng, sử dung dấu (->) để truy xuất tới
- Access modifier là từ khóa dùng để quy định mức độ truy cập đến lớp và các thành phần của lớp. Có 3 mức truy cập: 
  - public: có  thể truy cập bất cứ đâu
  - private: Các phương thức và thuộc tính chỉ có thể truy cập cùng 1 lớp
  - protected: Các phương thức và thuộc tính được phép truy xuất cùng 1 lớp và ở lớp con kế thừa.
- Getter và Setter truy cập trực tiếp vào trường dữ liệu
- Phương thức khởi tao constructor là phương thức giúp khởi tạo các đối t
