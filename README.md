***
# Module2-reflection-ngày 22/2
***
- String:
  + là kiểu dữ liệu cơ bản trong PHP
  + Là đãy liên tiếp các kí tự
  + Đươc bao quanh bơi dấu " ", và ' ' 
  + Chuỗi không có kí tự gọi là chuỗi kí tự rỗng,
- Một số hàm làm việc với chuỗi: 
  +  Strlen($string): Hàm trả về độ dài của chuỗi
  +  str_word_count($string): Hàm trả về số từ trong chuỗi
  +  str_replace($find, $replace, $string): Hàm tìm kiếm chuỗi $find, thay thế chuỗi đó bằng $replace trong chuỗi ban đầu ($string)
  +  trim($string, $charlist): Hàm có tác dụng loại bỏ khoảng trắng hoặc các ký tự $charlist trong chuỗi $tring.
  
  
- RegEx ( Regulation Expresstion ) Biểu thức chính quy:
  + Được hiểu đơn giản là một biểu thức dùng để mô tả một mẫu chuỗi nào đó
  + Được dùng để xử lý  chuỗi nâng cao qua biểu thức rieeng của nó, những biểu thức này có nghuyên tắc riêng của nó, những biểu thức này sẽ có nguyên tắc riêng và phải tuân theo nghuyên tắc đó thì biểu thức mới hoạt động.
- Tại sao lại dùng RegEx : 
  +  Đơn giản hóa việc xác định các mẫu trong chuỗi dữ liệu bằng cách gọi hàm duy nhất
  +  Xác thực dữ liệu người dùng nhập vào như password, ID...
  +  Dễ dàng từ khóa  trong tìm kiếm
  +  Tạo mẫu HTML hoàn chỉnh và tăng hiệu suất chương trình lên nhiều lần.
- Khai báo biểu thức chính quy: 
  + Để khai báo 1 chuỗi RegEx ta chỉ cần khai báo bắt đầu bằng kí tự / và kết thúc cũng là ký tự /.
  + Cú pháp : $pattern : '/các ký tự của RegEx - metacharacters/Flaf/';
- Một số kí tự cơ bản trong RegEx:
  + ^: bắt đầu bằng một chuỗi
  + $: kết thúc của chuỗi
  + *: 0 hoặc nhiều lần xuất hiện
  + +: 1 hoặc nhiều lần xuất hiện
  + ?: 0 hoặc 1 lần xuất hiện
  + .: Đại diện cho 1 kí tự bất kì
  + [] : Tìm tập hợp các chuỗi
  + \ : tìm kiếm giá trị đặc biệt
  + | : chọn giá trị A hoăc B => (A|B)

***
# Module2-reflection-ngày 19/2
***
- Xử lý ngoại lệ là khi luồng thực thi của một ứng dụng diễn ra không như ý muốn thông thường, thì được cho là ngoại lệ. Do đó, trong các chương trình phần mềm, chúng ta thường triển khai các cơ chế xử lí ngoại lệ để chương trình đảm bảo được các tình huống xảy ra.
- Để xử lý ngoại lệ, chúng ta sử dụng câu lệnh try/catch.Để sử dụng câu lệnh này, chúng ta viết khối try xung quanh các câu lệnh có thể xảy ra ngoai lệ đó. Sau đó chúng ta viết khối catch chứa các lệnh thực thi nếu có bất kì ngoại lệ xảy ra trong bất kì câu lệnh nào trong khối try
- Throw : Đây là cách kích hoạt 1 ngoại lệ> Mỗi "Throw" bắt buộc phải có 1 'catch' 
- Ví du:
-  function checkNum($number) {
    if($number>1) { <br>
    throw new Exception("Value must be 1 or below");<br>
   }<br>
   return true;<br>
   }<br>
   try {<br>
   checkNum(2);<br>
   echo 'If you see this, the number is 1 or below';<br>
 }<br>
 catch(Exception $e) {<br>
   echo 'Message: ' .$e->getMessage();<br>
 }<br>
 
 - Finally : Khối lệnh này luôn được thực hiện cho dù ngoại lệ có xảy ra hay không.
 - Ưu điểm của  ‘catch và throw’: 
   + Người lập trình chỉ xử lý ngoại lệ khi cần thiết. không cần thực hiện lại mọi mức.
   + Thông báo lối có thể được hiện ra khi xử lý ngoại lệ
 - Tác dụng : 
   + Chương trình chạy theo nghiệp vụ của mình
   + Cho biết chương trình lỗi chỗ nào, nghiệp vụ nào

***
# Module2-reflection-ngày 18/2
***
- Thuật toán sắp xếp (sorting)là quá trình bố  trí lại các phần tử của một danh sách đối tượng nào đó theo một trật tự nhất định. Chảng hạn như thứ tự tăng dần (hay giảm dần) đối với một dãy số, thứ tự từ điển đối với một dãy chữ... 

- Sắp xếp nổi bọt(bubble sort) :
   + là thuật toán đơn giản, với thao tác cơ bản là so sánh các phần tử liền kề nhau, nếu chúng chưa đứng đúng thứ tự thì đổi chổ cho nhau. Nó sử dụng phép so sánh các phần tử nên là một giải thuật sắp xếp kiểu so sánh.
   + Giải thuật này không thích hợp sử dụng với các tập dữ liệu lớn khi mà độ phức tạp trường hợp xấu nhất và trường hợp trung bình là Ο(n2) với n là số phần tử.

- Sắp xếp chèn (Insertion Sort) :
   + Là chèn thêm một phần tử vào danh sách con đã qua sắp xếp. Phần tử được chèn vào vị trí thích hợp sao cho vẫn đảm bảo rằng danh sách con đó vẫn sắp theo thứ tự
   + Giải thuật này không thích hợp sử dụng với các tập dữ liệu lớn khi độ phức tạp trường hợp xấu nhất và trường hợp trung bình là Ο(n2) với n là số phần tử.

- Giải thuật sắp xếp chọn (Selection Sort)
   + Là thuật toán dựa trên việc so sánh tại chỗ ,sắp xếp một mảng bằng cách liên tục tìm phần tử tối thiểu, từ phần không được sắp xếp và đặt nó ở đầu. Thuật toán duy trì hai mảng con trong một mảng nhất định.
      + Mảng con đã được sắp xếp
      + Mảng con còn lại chưa được sắp xếp
   + Trong mỗi lần sắp xếp lựa chọn, phần tử tối thiểu từ mảng con chưa được sắp xếp được chọn và chuyển đến mảng con đã được sắp xếp.
   + Giải thuật này không phù hợp với tập dữ liệu lớn khi mà độ phức tạp trường hợp xấu nhất và trường hợp trung bình là O(n2) với n là số phần tử.
  
***
# Module2-reflection-ngày 17/2
***
- Tìm kiếm tuyến tính (Linear Search):
  + Hay còn gọi là thuật toán tìm kiếm tuần tự là một phương pháp tìm kiếm một phần tử cho trước trong một danh sách bằng cách duyệt lần lượt từng phần tử của danh sách đó cho đến lúc tìm thấy giá trị mong muốn hay đã duyệt qua toàn bộ danh sách.
  + Đặc điểm cơ bản của nó là rất đơn giản khi giải thuật, khá tỏ ra hiệu quả khi cần tìm kiếm trên một danh sách đủ nhỏ hoặc danh sách chưa sắp xếp thứ tự đơn giản.    
- Tìm kiếm nhị phân (Binary Search): 
  + Hay còn gọi là thuật toán tìm kiếm một nửa, bắt đầu với một khoảng từ phần tử đầu mảng, tới cuối mảng. Nếu giá trị của giá trị cần tìm nhỏ hơn giá trị của phần tử nằm ở giữa khoảng thì thu hẹp phạm vi tìm kiếm từ đầu mảng tới giữa mảng và ngược lại. Cứ thế tiếp tục chia pham vi thành các nửa cho đến khi tìm thấy hoặc đã duyệt hết.
  + Thuật toán tìm kiếm nhị phân tỏ ra tối ưu hơn so với tìm kiếm tuyến tính ở các mảng độ dài lớn và đã được sắp xếp. Ngược lại, tìm kiếm tuyến tính sẽ tỏ ra hiệu quả hơn khi triển khai trên mảng nhỏ và chưa được sắp xếp.


# Module2-reflection-ngày 5/2
***
- Bộ thư viện SPL (Standard PHP Libary) cung cấp nhiều dữ liệu tiêu chuẩn để chúng ta có thể sử dụng ngay trong ứng dụng của mình. Các cấu trúc dữ liệu này được phân thành các nhóm dựa vào hình thức triển khai của chúng, và cũng căn cứ vào cách sử dụng của chúng trong các tình huống thực tế
- Các thành phần của SPL :
  +  Predefined Constants là danh sách các hằng số :số pi, số E,...
  +  Datastructures chứa danh sách các lớp co khả năng làm việc với cấu trúc, dữ liệu khác nhau LinkList, Stack, Queue, Heaps,...
  +  Interator: Chứa các lớp cho phép có khả năng thực hiện các phép lặp để duyệt các cấu trúc khác nhau tùy vào cấu trúc dữ liệu.
  +  Danh sách các Interface
  +  Exception là danh sách điều khiển các lớp ngoại lệ
  +  File Handling cung cấp các lớp làm việc với file trong hệ thống.
  +  SPL Funtions cung cấp các hàm hỗ trợ cần thiết.
  +  Miscellaneous Classes và Interface.
- Double LinkedList ( danh sách liên kết dodoi):
  + Một danh sách liên kết đôi là một danh sách các NODE được liên kết với nhau theo 2 hướng. 1 số DS liên kết đồi bao gồ
      +  SplDoublyLinkedList
         + SplStack
         + SplQueue       


# Module2-reflection-ngày 4/2
***
- Stack
  +  là một cấu trúc dữ liệu danh sách, trong đó việc thêm và lấy được thực hiện theo quy tắc FILO(Firt-In/Last-Out), có nghĩa là phần tử nào đầu tiên sẽ được lấy sau cùng. Nguyên tắc này cũng được gọi là LIFO (Last-In/First-Out), có nghĩa là phần tử nào được đưa vào sau cùng sẽ lấy ra đầu tiên
  +  Các thao tác thông dụng của stack: 
     +  init : Khởi tạo stack
     +  Push : thêm 1 phần tử vào stack
     +  Pop : Loại bỏ phần tử cuối cùng được thêm vào đầu stack
     +  isEmpty : Kiểm tra stack có trống hay không
     +  top : Lấy ra giá trị đầu tiên của stack
- Queue 
   + là một cấu trúc dữ liệu danh sách, Việc thêm và lấy theo quy tắc FIFO(Firt-in/Firt-out), phần tử thêm vào đầu tiên sẽ lấy đầu tiên, Cũng gọi là nguyên tắc LILO-thêm vào sao cùng lấy ra sau cùng.
   + các thao tác thông dụng: 
      +  init: khởi tạo một hàng đợi
      +  enqueue: thêm 1 phần tử vào cuối
      +  dequeue: Lấy ra phần tử đầu tiên
      +  isEmpty: trả về true/false xem hàng đợi này có chứa phần tử nào ko.
 - Cấu trúc cây (tree) 
      +  Là một cấu trúc dữ liệu gồm một tập hợp hữu hạn các nút,  giữa các nút có 1 mối quan hệ "cha-con". Có một nút đặc biệt gọi là gốc (root)

 -  Duyệt qua các phần tử của tree
      +   pre-order - duyệt node hiện tại rồi sau đó sang cây bên trái và cây bên phải
      +   in-order (đối xứng) - duyệt bên trái trước, sau đó duyệt node hiện tại, rồi duyệt node bên phải
      +   post-order - duyệt bên trái trước, sau đó bên phải, rồi duyệt node hiện tại
      +   level-order (duyệt theo bề rộng) - duyệt node hiện tại, sau đó duyệt tất cả các node anh em (siblings), rồi chuyển sang duyệt những node ở level tiếp theo

# Module2-reflection-ngày 3/2
***
- Cấu trúc dữ liệu là cách lưu trữ, tổ chức dữ liệu có thứ tự, có hệ thống dữ liệu để dữ liệu có thể sử dụng một cách hiệu quả.
- Đặc điểm  của cấu trúc dữ liệu là: 
   + Chính xác
   + Độ phức tạp về thời gian :  thời gian chạy hay thời gian thực thi phải nhở nhất có thể
   + Độ phức tạp về bộ nhớ : Sử dụng bộ nhớ của mỗi phép tính dữ liệu nên là nhỏ nhất có thể
 - Cấu trúc dữ liệu ArrayList:
   + Là một cấu trúc dữ liệu danh sách đặc trưng, bên trong ArrayList sử dụng mảng để lưu trữ dữ liệu.
   + Thao tác với ArrayList là chậm vì nó dùng nội bộ mảng. Nếu bất kỳ phần tử nào được xóa khỏi mảng , tất cả các bit được chuyển trong bộ nhớ
   + Tốt hơn trong việc lưu trữ và truy cập dữ liệu nhờ việc truy xuất nhanh đến các phần tử, nhờ có  cơ chế truy xuất ngẫu nhiên của 1 mảng.
 - LinkedList :
   + Là một cấu trúc dữ liệu danh sách, các phần tử liên kết qua các tham chiếu tuyến tính giữa các phần tử liên tiếp nhau.
   + So với ArrayList thì thao tác của Linked nhanh hơn bởi vì nó sử dụng danh sách liên kết, do đó không cần chuyển đổi bit nào.
   + Vì thao tác dữ liệu nhanh nên các thao tác thêm sửa xóa phần tử trong LinkedList lại rất hiệu quả, bởi vì chỉ cần thay đổi tham chiếu phần tử
   
   
# Module2-reflection-ngày 2/2
***

- Clean code:
  +  Giúp công việc cộng tác nhóm, dễ hiểu code, đơn giản dễ đọc.
  +  Dễ thay đổi, bảo trì, cải tiến.
  +  Đáp ứng được tính logic
- Các cách thực hành clean code
  + Đặt các tên lớp, phương thức và biến thích hợp. Chúng phải đơn giản và có ý nghĩa và đáp ứng được ba mục đích: nó làm gì, tại sao nó tồn tại và cách nó được sử dụng.
  + Nhiều LTV thường hay viết những đoạn code quá phức tạp. Họ giao quá  nhiều trách nhiệm trong một lớp, điều này làm nó phức tạp khó duy trì vì vậy chỉ giao nhiệm vụ duy nhất cho một class
  + Commen code rất quan trong, giúp chúng ta tiết kiệm được rất nhiều thời gian.
  + Review code: 
    +  1 hàm không nên quá 30 dòng.
    +  Lớp không lên vượt quá 500 dòng
    + 1 dòng không nên dài quá 80 kí tự
    + 1 dòng chỉ chứa 1 biến
    + 1 hàm không vượt quá 5 tham số
 
- Refactoring code
  + Giúp code dễ đọc, dễ tìm hiểu, dễ tiếp cận hơn từ đó nó sẽ giúp chúng ta dễ bảo trì, mở rộng hệ thống.
- SOLID là gif?
  + Là viết của 5 chữ cái đầu tiên trong 5 nguyên tắc thiết kế hướng đối tượng. Giúp cho LTV viết ra những đoạn code dễ đọc, dễ hiểu.
  + 5 nguyên tắc bao gồm : 
    +  Single responsibility priciple: Mỗi lớp chỉ nên chịu trách nhiệm về một nhiệm vụ cụ thể nào đó. Nếu có quá nhiều chức năng sẽ trở lên khó đọc.
    +  Open/Closed principle : Không được sửa đổi một Class có sẵn, nhưng có thể mở rộng bằng kế  thừa. Theo nghuyên lý này, nếu muốn thêm chức năng cho chương trình, chúng ta nên viết class mới mở rộng class cũ ( bằng cách kế thừa hoặc sở hữu class cũ ).
    + Liskov substitution principle: Các đối tượng (instance) kiểu class con có thể thay thế các đối tượng kiểu class cha mà không gây ra lỗi.
    + Interface segregation principle : Thay vì dùng 1 interface lớn, ta nên tách thành nhiều interface nhỏ, với nhiều mục đích cụ thể.
    + Dependency inversion principle: 
          + Các module cấp cao không nên phụ thuộc vào các modules cấp thấp. Cả 2 nên phụ thuộc vào abstraction.
          + Interface (abstraction) không nên phụ thuộc vào chi tiết, mà ngược lại (Các class giao tiếp với nhau thông qua interface (abstraction), không phải thông qua implementation.)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 1/2
***
<h3> Abstrack Class là gì: </h3>
   -  Lớp trừu tượng được xem như 1 class cha cha tất cả các class nó cùng bản chất, và phải dùng từ khóa extends<br>
   -  Không cho phép có các  tham số chỉ khai báo các thuộc tính và phương thức bình thường.<br>
   -  Các phương thức định nghĩa abstract trong abstract class chỉ khai báo tên hàm và không viết nội dung hàm đó. Nội dung sẽ đươc viết trong class kế thừa khi override lại phương thức đó<br>
     Ví dụ <br>
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
<h3> Interface là gì : </h3>
    -  Không phải là một lớp. Nó được mô tả như một bản thiết kế cho các class có chung cách thức hoạt động. <br>
    -  Không phải một lớp lên nó không định nghĩa thuộc tính và khởi taọ đối tượng mà chỉ khai báo phương thức <br>
    -  Các phương thức chỉ khai báo tên hàm và không viết nội dung hàm trong đó.<br>
    -  Không có khái niệm phạm vi phương thức, tất cả là public<br>
    -  Lớp con kế thừa interface sẽ phải ghi đè tất cả phương thức trên đó<br>
    -  Có thể kế thừa nhiều interface khác nhau bằng từ khóa implements.<br>
 ví dụ:<br>
      <?php<br>
      interface Move <br>
   {<br>
       function run();<br>
   }<br>
      class Dog implements Move<br>
   {<br>
       public function run () <br>
        echo "Con chó chạy nhanh";<br>
    }<br>

<h3> Khi nào dùng interface và khi nào dùng abstract Class. </h3><br>
Nhìn chung cả 2 đều được coi như là một bản thiết kế cho các class con kế thừa nó<br>
     Abstract class là bản thiết kế cho class: <br>
       -  Về bản chất abstract class là một bản class khai báo thêm các thuộc tính và phương thức khác không phải trừu tượng.
         nó được xem như bản thiết kế cho class vì những class extends lại từ nó ngoài override lại các phương thức trừu tượng 
         của nó thì có thể sử dụng nó.<br>
       -  Abstract thường được sử dụng trong trường hợp class kế thừa từ nó cùng bản chất<br>
     Interface là "bản thiết kế" cho Method:<br>
       -  Vì những class implements đều ghi đều phải override lại phương thức của nó<br>
       -  Interface thường được sử dụng trong trường hợp các kế  thừa không có cùng bản chất như nhau

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
