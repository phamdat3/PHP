## Tim hiểu về PHP
---
  Thực hiện: **Phạm Văn Đạt**

  Cập nhập lần cuối: *4/3/2017*

# Mục lục 
[1. Giới thiệu về PHP](#1)        
[2. Nhúng PHP vào trang HTML](#2)   
[3. Biến và chú thích](#3)   
[4. Cấu hình Web Server](#4)   
[5. Hàm phpinfo()](#5)                
[6. Định dạng code (indentation)](#6)     
[7. Sử dụng echo, print](#7)      
[8. echo_print mã html](#8)                 
[9. Biểu thức nối chuỗi(concatenation)](#9)      
[10. Nhúng PHP vào trang HTML](#10)          
[11. Biểu thức điều kiện if else](#11)           
[12. Biểu thức điều kiện if else if else](#12)          
[13. Biểu thức gán](#13)        
[14. Biểu thức toán học](#14)                                      
[15. Toán tử tăng và gảm(increment and decrement operator)](#15)       
[16. Biểu thức so sánh](#16)             
[17. Biểu thức quan hệ(logic)](#17)                     
[18. Hàm die và exit](#18)                
[19. Vòng lặp While](#19)                   
[20. Vòng lặp for](#20)                
[21. Break và continue](#21)                   
[22. Cấu trúc rẽ nhánh Switch](#22)                    
[23. Expression matching](#23)                    
[24. Hàm(fuction)](#24)                    
[25. Hàm với tham số](#25)               
[26. Hàm với giá trị trả về](#26)               
[27. Biến toàn cục và biến cục bộ](#27)                              
[28. Phương thức GET và POST trong php](#28)                
[29. Các hàm xử lý chuỗi trong php](#29)                   
[30. Giải thuật đệ quy trong php](#30)                
[31. Các hàm xử lý mảng trong php](#31)                   
[32. Các hàm xử lý file trong php](#32)                    
[33. Expression matching](#33)                    
[34. Upload file lên server với php](#34)                    
[35. Các hàm kiểm tra dữ liệu trong php](#35)               
[36. Session và cookie trong php](#36)               
[37. Hàm isset() và empty() trong php](#37)                 
[38. Xử lý truy vấn dữ liệu MySQL với PHP](#38)                
[39. Lệnh require - require_once - include - include_once trong PHP](#39)                   
[40. Xử lý ngày tháng trong PHP](#40)                
[41. Các hàm xử lý mảng trong php](#41)                   
[42. Tìm hiểu hàm header trong PHP](#42)                    
[43. PHP Filter - Hàm filter_var trong PHP](#43)                    
[44. Header Request và Header Response](#44)                    

# Nội dung.
<a name="1"></a>
## 1. Giới thiệu về PHP
- **PHP** (Hypertext Preprocessor) là một ngôn ngữ lập trình kịch bản hay một loại mã lệnh chủ yếu được dùng để phát triển các ứng dụng viết cho máy chủ(server), mã nguồn mở, dùng cho mục đích tổng quát. Nó rất thích hợp với web và có thể dễ dàng nhúng vào trang HTML. Do được tối ưu hóa cho các ứng dụng web, tốc độ nhanh, nhỏ gọn, cú pháp giống C và Java, dễ học và thời gian xây dựng sản phẩm tương đối ngắn hơn so với các ngôn ngữ khác nên PHP.
- Để tạo một trang Web động thì ta cần sử dụng ngôn ngữ PHP và hệ quản trị cơ sở dữ liệu (ví dụ như SQL) 
- Để có thể thử cá đoạn code về web của chúng ta môt cách giễ dành thì chúng ta không thể nào mà đẩy chũng lên website để thử vì nó khá tốn công và tốn thời gian. Vì thế chũng ta nên tạo 1 web server ảo trên chính máy của chũng ta để thử và khi đã ổn định rồi thì chũng ta mới đẩy lên.
- Có hai loại web server ảo phổ biến là **wampp** và **xampp** chũng ta hãy tải 1 trong hai về để cài đặt và sử dụng.
- Sau khi cài đặt song chũng ta hay truy cập vào rang web **localhost**

<img src="http://imageshack.com/a/img921/138/FNV29t.png">
- Tạo một trang PHP cow bản:

 + Tạo một file để viết PHP với đường dẫn là `Local Disk(C:)\wamp\www` và có đuôi là `.php`  

 + Viết một đoạn với thẻ đóng mở:  
 <img src="http://imageshack.com/a/img922/6791/HBVXgb.png">
 + Sau đó trúng ta ra trang web **localhost** chũng ta gõ thêm vào là *localhost/ten_file.php*
 <img src="http://imageshack.com/a/img923/5499/N0kPkq.png">
 <img src="http://imageshack.com/a/img922/855/6XwSeW.png">

<a name="2"></a>
## 2. Nhúng PHP vào trang HTML
- File được lưu phải có đuôi là `.php` thì mới có thể nhúng PHP vào trang HTML, nếu không để đuôi đó thì nó xẽ bỏ qua luôn không được đọc đoạn PHP đó.
- **echo**: là hàm để in ra một chuỗi dạng text, thẻ HTML. Nội dung cần hiển thị có thể nằm trong dấu nháy đợn hoặc nháy kép.
- **print**: cũng tương tự như hàm **echo**, có thể in ra thêm các định dạng.

<a name="3"></a>
## 3. Biến và chú thích
- Cài Web server. Sau đó bật lên và lên trình duyệt truy cập vào trang `localhost`.
- Tạo một thư mục trong thư mục `www`.
- Commen: Không có hiệu lục gì khi viết code chỉ để giải thích.
   + Dùng dấu `\\` thì dòng dduocj đánh dấu đó sẽ là comments
   + Dùng dấu `\* nội dung *\` thì phàn nội dung ở trong sẽ là comments
   + Dùng dấu `#` thì dòng đó sẽ là commen.
- Kết thúc mỗi câu lệnh là dấu `;`
- Câu lệnh **echo** xuất ra màn hình.
- Dấu **$** là phần tử bắt buộc phải có khi khai báo biến.
- Biến như là một cái hộp để đựng những giá trị cần thiết. Khi khai báo biến thì nó được cấp cho một vùng nhớ và nó có thể lưu trữ hay gán giá trị vào và có ý nghĩa trong xuất chương trình. Biến này có thể thay đổi giá trị trong quá trình sử dụng và nó có tác dụng khi bắt đầu đến dòng thay đổi biến.
- Chú ý: Không cần pahir khai báo kiểu dữ liệu của biến khi khai báo, mà gán thẳng giá trị cho biến đó và nó xẽ ngầm định dạng cho kiểu biến. Không giống như các ngôn ngữ khác.
- Cú pháp khai báo biến  mảng 1 chiều: 
```
 $myArr = array("5","3","2");
 echo $myArr[2]; // truy xuất phần tử thứ 3, có giá trị hiển thị là 2
```
- Cú pháp khai báo mảng 2 chiều:
```
 $myTwoDimension = array(array(a,b,c),array(3,4,6));
 echo $myTwoDimension[0][1]; // truy xuất đến biến có giá trị hienr thị là **b**.
```

<a name="4"></a>
## 4. Cấu hình Web Server
- Nếu bạn có cài một số phầm mềm khác phần mềm bạn đang cài mà chưa gỡ bỏ hoàn toàn thì nó xẽ bị lỗi xung đọt cổng với nhau khi bạn vào **localhost**.
**Chú ý** Nếu bạn bị sung đột cổng mới thay đổi còn không thì chũng ta không nên thay đổi.
- Cách giải quyết:
 + Vào thư mục **bin/apache/apache2.4.23/conf** 
 + Vào thư mục **htppd.conf** để sửa một số thông tin có liên quan về cổng.
 + Đi đến dòng có hiển thị: 

<img src="http://imageshack.com/a/img923/5220/8leeZF.png">
 + Thay đổi:
<img src="http://imageshack.com/a/img923/8556/ltbdTj.png">
 + Lưu lại và khỏi động lại.
 + Chúng ta thử đăng nhập vào localhost. Giờ chũng ta không đăng nhập vào đường dẫn là **localhost** mà chũng ta phải đăng nhập vào **loaclhost:30** (chúng ta đã sử thành 30).
- Thay đổi thư mục lưu trữ các code mình viết.

<a name="5"></a>
## 5. Hàm phpinfo()

<a name="6"></a>
## 6. Định dạng code (indentation)
- Việc PHP tự tìm ra lỗi là hơi khó nên khi ta viết mã code thì phải phân bố cục từng phần thụt ra và thụt vào hợp lý cho dễ dàng nhìn từng phần một. Để khi ta tìm lỗi hay sửa lỗi thì dễ dàng hơn.
- Chú ta có thể dùng thêm các comments để dễ hiểu từng phần hơn

<a name="7"></a>
## 7. Sử dụng echo, print
- **echo**: là hàm xuất một chuỗi ra màn hình web.
- **print**: tương tụ hàm echo.
- Nhưng hàm echo dduocj sử dụng nhiều hơn.

<a name="8"></a>
## 8. echo_print mã html
- Có thể Chèn PHP vào HTML để dùng hàm echo rồi in ra màn hình.

<img src="http://imageshack.com/a/img921/8999/LxZV2U.png">
- Vì bây giờ đoạn văn bản in ra là dùng theo PHP nên ta có thể chèn thêm biến bất kỳ vào trong đoạn vă bản được.
<img src="http://imageshack.com/a/img921/3218/EsOYot.png">
- Dùng if else để in ra tùy chọn:
<img src="http://imageshack.com/a/img923/4956/xTiL80.png">
- Có thể thêm css vào nữa:
<img src="http://imageshack.com/a/img921/264/jymbsA.png">
- Dấu `" " ` và dấu `' '` trong khai báo biến và trong hàm echo là tương đương nhau, chú ý là dung dấu mở nào thì phải dùng dấu đóng tương ứng.
- Để in ra dấu `'` hoăc dấu `"` nằm trong dấu tương ứng của nó thì chúng ta phải sử viết là `\'` và `\"`.
<img src ="http://imageshack.com/a/img923/7436/zILSld.png">

<a name="9"></a>
## 9. Biểu thức nối chuỗi(concatenation)
- Để 2 chuỗi khi xuất ra màn hình cách nhau bởi một dấu cách thì chúng ta dùng `$bien1.' '.$bien2`. Dấu `.` có thể thay bằng dấu `,`.

<img src="http://imageshack.com/a/img924/6696/exIWoT.png">
<img src="http://imageshack.com/a/img922/3632/BEaiwW.png">
- Nối thêm một đoạn vào nữa thì dùng `$bien .= "noi dung them";`

<a name="10"></a>
## 10. Nhúng PHP vào trang HTML
- Khai báo trên cùng chủ yếu nên khai bảo biến, mảng,kết nối... muốn sử dụng trong chương trình.
- Ở giữa chủ yếu để đưa ra kết quả và html format.

<img src="http://imageshack.com/a/img922/8394/ZXJAdt.png">
- Ở cuối chủ yếu dùng để hủy giá trị biến, mảng, kết nôi

<a name="11"></a>
## 11. Biểu thức điều kiện if else
- Nếu trong câu điều kiện chỉ có 1 lệnh thì khong cần dấu ngoặc `{}` nếu từ 2 lệnh trở lên thì cần phải có dấu ngoặc.
- Với câu điều kiện if else lồng nhau thì phải chú ý đền các dấu ngoặc.

<a name="13"></a>
## 13. Biểu thức gán
- Chungs ta có thể gán giá trị cho biến theo nhiều cách.
  + Gán thẳng cho biến luôn:
  
<img src="http://imageshack.com/a/img924/741/kFkCYE.png">
  + Gán thông qua biến khác:
<img src="http://imageshack.com/a/img922/4641/uvSlfB.png">
  + Chúng ta còn có thể gán được cả phép tóan cho biến:
<img src="http://imageshack.com/a/img924/2075/SNLmh4.png">

<a name="14"></a>
## 14. Biểu thức toán học
- Chúng ta có thể thục hiện các phép toán như trên các ngôn ngữ khác để có thể tính toán như bình thường. 
chú ý phép `/` là phép lấy giá trị nguyên, phép `%` là phép lấy số dư.

<img src="http://imageshack.com/a/img924/4691/GcoEvd.png">

<a name="15"></a>
## 15. Toán tử tăng và gảm(increment and decrement operator)
- Khi chúng ta dùng `$a++ hoặc $a--` nghĩa là chúng lấy giá trị của **a** trước để in ra hoặc dùng cho các phép toán trước rồi nó mới tăng hoạc giảm giá trị cảu nó sau.
- Khi chúng ta dùng `++$a hoặc --$a` là chúng ta tăng hoạc giảm chũng trước rồi in ra hoặc dùng để tính toán.

*Chúng ta phải đặc biệt chú ý đến 2 cơ chế hoạt động cảu 2 trường hợp này*

<img src="http://imageshack.com/a/img924/4889/TZ0Esx.png">

<img src="http://imageshack.com/a/img922/7024/sAmZ2Z.png">

<a name="16"></a>
## 16. Biểu thức so sánh
- So sánh giá trị của hai biến.

<img src="http://imageshack.com/a/img922/1231/OQv1k5.png">
- So sánh  kiểu dữ liệu của ha biến `===`.
<img src="http://imageshack.com/a/img923/4831/5ZeoTT.png">
<img src="http://imageshack.com/a/img923/6172/i8mxtG.png">

<a name="17"></a>
## 17. Biểu thức quan hệ(logic)
- Dạng 1: biểu thức quan hệ **end** ký hiệu là `&&`.

<img src="http://imageshack.com/a/img921/2171/7QKHaN.png">
- Dạng 2: Biểu thức quan hệ **or** ký hiệu là `||`.
<img src="http://imageshack.com/a/img922/7167/T2018P.png">

<img src="http://imageshack.com/a/img922/6418/nRGMdM.png">
- Dạng 3: Biểu thức quan hệ **xor**.
<img src="http://imageshack.com/a/img921/6038/27bJIq.png">

<a name="18"></a>
## 18. Hàm die và exit
- Dùng để thoát khỏi chương trình và thông báo cho người dùng biết có một lỗi nào đó. Và đưa ra lỗi cho người dùng biết.
- Ban đầu.

<img src="http://imageshack.com/a/img924/4586/M5ZHUO.png">
 + Khi cho thêm hàm `die`. Thì các dòng lệnh sau thẻ `die` sẽ không được đọc đến và k được biên dịch ra mà chỉ bien dịch và dữ lại các câu lệnh trước thẻ `die`.

<img src="http://imageshack.com/a/img923/944/aRhUYE.png">

 + Khi cho thêm thẻ `exit`. Thì các dòng lệnh sau thẻ `exit` sẽ không được đọc đến và chỉ đọc đk những thẻ trước nó và không được lưu dữ lại àm ó sẽ thoát ra khỏi luôn.

<img src="http://imageshack.com/a/img923/5084/Lcpj5r.png">

<a name="19"></a>
## 19. Vòng lặp While và do while.
- Vòng lặp do while: Thực hiện câu lệnh trước rồi kiểm tra điều kiện, nên số lần lặp ít nhất là 1.

<img src="http://imageshack.com/a/img923/7771/0j2mFZ.png">
- Vòng lặp While: Thực hiện kiểm tra điều kiện trước sau đó mói thực hiện lệnh, nên số lần lặp ít nhất là 0.
<img src="http://imageshack.com/a/img923/7106/W3DusA.png">

<a name="20"></a>
## 20. Vòng lặp for
- Vòng lặp mà chúng ta có thể kiểm xoát được biến khỏi tạo dan đầu và số vòng lăp và lặp như thế nào ngay từ đâu.

<img src="http://imageshack.com/a/img924/2610/SAUazw.png"> 

<a name="21"></a>
## 21. Break và continue
- **Break**: Dừng công việc (vd như dừng vòng lặp) và thoát khỏi và không đọc các lênh phái sau.

<img src="http://imageshack.com/a/img924/5927/RRpoB8.png">
- **Continue**: Tiếp tục các câu lệnh phía sau.
<img src="http://imageshack.com/a/img924/2694/0gBJ7U.png">

<a name="22"></a>
## 22. Cấu trúc rẽ nhánh Switch
- Bắt niến nào đó trong nhiều trường hợp.

<img src="http://imageshack.com/a/img924/1776/szXW1k.png">
- Chú ý: Switch chỉ so sánh bằng không có so sánh lớn hơn hoặc nhỏ hơn.

<a name="23"></a>
## 23. Expression matching
- Kiểm tra tính hợp lệ của dữ liệu. Sử dụng hàm `preg_match`
- Các dùng hàm **preg_match**: `(preg_match('/ky_tu_can_tim_trong_chuoi/', $bienchuoi))`

<img src="http://imageshack.com/a/img922/7537/DTm3mF.png">
<img src="http://imageshack.com/a/img923/9702/lpgbKC.png">
- Tìm ký tự nằm trong khoảng nào đó.
<img src="http://imageshack.com/a/img923/1083/Jq1A2d.png">
<img src="http://imageshack.com/a/img922/6244/nlR0sr.png">
- Kiểm tra ký tự đầu tiên
<img src="http://imageshack.com/a/img922/360/exkWZy.png">
<img src="http://imageshack.com/a/img923/5765/o5Vaa5.png">
- Kiểm tra ký tự kết thúc
<img src="http://imageshack.com/a/img924/6122/0YFhlv.png">
<img src="http://imageshack.com/a/img923/6109/9avw9i.png">

<a name="24"></a>
## 24. Hàm(function)
- Khai báo hàm `function ten_ham(){.....}`
- Lời gọi hàm `ten_ham();`

<img src="http://imageshack.com/a/img923/8916/k3afMV.png">

<a name="25"></a>
## 25. Hàm với tham số

<a name="26"></a>
## 26. Hàm với giá trị trả về
- Có thể trả về dược cả số và chuỗi ký tự.

<img src="http://imageshack.com/a/img924/1617/ju0oag.png">
<img src="http://imageshack.com/a/img923/315/e6ab1R.png">

<a name="27"></a>
## 27. Biến toàn cục và biến cục bộ
- Biến toàn cụ là biến sử dụng trong toàn bộ bài code, muốn sử dụng bến toàn cục để dùng trong một hàm nào đó thì ta có 2 chách:
 + Sử dụng **global**
 
<img src="http://imageshack.com/a/img922/9812/iY84XJ.png">
 + Sử dụng biến **$GLOBALS['']**
<img src="http://imageshack.com/a/img924/1606/B3KFvr.png">
- Biến cục bộ là biến chỉ sử dụng được trong hàm chứ nó. Nghĩa là nó chỉ được dùng trong vùng dấu **{ }** chứa nó.

<a name="28"></a>
## 28. Phương thức GET và POST trong php
* Phương thức get.
     * Là phương thức lấy dữ liệu qua đường đẫn URL. Server nhận và phân tích dữ liệu nhữ gì nằm sau dấu *?* là hững thứ mà client gửi lên.
* Server nhận dữ liệu
     * Tất cả dữ liệu mà Client gửi lên đều đươc Server lưu trong một biến cục bộ **$_GET** dạng mảng và theo quy luật **key=>value**
     * Ví dụ:
 Cho đoạn Code
```
<?php 
foreach ($_GET as $bien => $gt)
{
    echo "$bien  =>  $gt <br/>";
}
?>
```
 Ta gõ đường dẫn `http://localhost/git.php?1=2&3=g`
Ta được.

<img src="http://imageshack.com/a/img922/1764/TI9l6s.png">

* Phuong thức post
  Phương thức post có tính bảo mật cao hơn vì Client gửi dữ liệu lên thông qua Form nên nó bị ẩn đi.
* Client gửi lên
 Phương thức post gửi dư liệu lên thông qua Form đăng nhạp HTML các giá trị đó được định nghĩa trong input gồm các kiểu (textbox,radio, password, textarea, hidden) và được nhận dạng thông qua name của input đó.
* Server nhận dữ liệu
 Tương tụ như get thì post ũng lưu dữ liệu vào biến cục bộ $_POST do PHP tạo ra.
 Để lấy dữ liệu ta làm như sau.
```
  if (isset($_POST['id']))
  {
    $id = $_POST['id'];
  }
```
 **Chú ý:** hàm isset($bien) dùng để có dữ liệu hay k.
* Ví dụ: Tạo thư mục post.php trong server.
```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>
        <form method="POST">
            Username: <input type="text" name="tên" value=""/> <br/>
            password: <input type="password" name="password" value=""/><br/>
            <input type="submit" name="form_click" value="Gửi"/>
        </form>
        <?php
                if (isset($_POST['form_click'])){
                    echo 'Tên đăng nhập là: ' . $_POST['tên'];
                    echo '<br/>';
                    echo 'Mật khẩu là: ' . $_POST['password'];
                }
           ?>
    </body>
</html>
```
* Ta đăng nhập vs đường dẫn `http://localhost/post.php` chúng ta đăng nhập vào form sau đó nhấp **Gửi** rồi xem kết quả.

<img src="http://imageshack.com/a/img922/6361/lo65x4.png">

* So sánh gửi Get và Post

|      | Post | Get |
|------|------|-----|
| **Giống nhau**| Gửi dữ liệu lên server | Gửi dữ liệu lên server |
|**Khác nhau**| Bảo mật hơn, không nhìn thấy bằng mắt thương| Kém bảo mật có thể nhìn thấy bằng mắt thường|
|          | Không tường minh | Tường minh|
|          | Chận hơn vì cần phải gửi lên Server để duyệt | Nhanh hơn vì nó được kiểm tra trên Brower|
|**Khi nào dùng Get / Post**| Dữ liệu cần bảo mật, | ít bảo mật và dữ liệu bạn muốn quảng bá|

<a name="29"></a>
## 29. Các hàm xử lý chuỗi trong php
Ví dụ:
```
$str = "đang ăn tối";
echo "Nam nói\"Cậu ấy $str\" "
```
Ở ví dụ này chúng ta cần chú ý đến dấu `/` và dấu `"` nằm cho đúng vị trí để chuỗi được nối đơn giản.
** Các hàn sử lý chuỗi hay sử dụng**
* addcslashes($str,$char_list) . Thêm dấu '/' vào trc các ký tự trong chuỗi $str mf ta liệt kê ở $char-list.
```
/ a..z là gồm các từ từ a => z
echo (addcslashes('freetuts.net FREETUTS.NET', 'a..z'));
// kết quả: \f\r\e\e\t\u\t\s.\n\e\t
  
echo '<br />';
  
// a..zA..Z là gồm các từ từ a => z và A => Z
echo (addcslashes('freetuts.net FREETUTS.NET', 'a..zA..Z'));
```
* addslashes($str) . Thêm dấu `/` trc các ký tự `',",\` trong chuỗi $str
```
echo addslashes ("Freetuts's a website learning online");
// Kết quả là Freetuts\'s a website learning online
```
* stripslshes($str). Xóa các ký tự `\`trong chuỗi $str
```
echo stripslashes("Mot so ham \\'xu ly \chuoi' trong PHP");
// Kết quả Mot so ham 'xu ly chuoi' trong PHP
```
* crc32($str). chuyển chuỗi thàng một dãy số.
```
echo crc32 ('freetuts.net');
// kết quả: -838644060
```
* explode($delimiter,$string). Hàm này chuyển chuỗi $string thành một mảng các phân tử mản là $delimiter
```
<?php

$str = 'freetuts.net is a website free for you';
  
var_dump(explode(' ', $str));
  
/*Kết quả
C:\wamp64\www\post.php:5:
array (size=7)
  0 => string 'freetuts.net' (length=12)
  1 => string 'is' (length=2)
  2 => string 'a' (length=1)
  3 => string 'website' (length=7)
  4 => string 'free' (length=4)
  5 => string 'for' (length=3)
  6 => string 'you' (length=3)
*/
?>
```
* implode($delimiter,$piecesarry). Chuyển mảng $piecesarry thành chuỗi.
```
echo implode(' ', array(
    'freetuts',
    'xin',
    'chào',
    'các',
    'bạn'
));
// kêt quả là freetuts xin chào các bạn
```
* ord($string) . Trả về mã ASCII của ký tự đầu tiên của chuỗi $string
```
echo ord ('Ab');
// kết quả: 65
```
* strlen($string) . Đếm số ký tự trong chuỗi
```
echo strlen('freetuts.net');
// kết quả: 12
```
* str_work_count($str) . trả về số từ trong chuỗi
```
echo str_word_count('freetuts xin chào các bạn');
// kết quả là 5
```
* str_repeat($str,int$n) . hàm lặp chuỗi $str$n lần
```
echo str_repeat( 'Hello', 5 );
// Kết quả là HelloHelloHelloHelloHello
```
* str_replace($chuoitim,$chuoithaythe,$chuoinguon) . Tìm kiếm và thay thế chuỗi
```
$str = 'Freetuts Xin Chào Các Bạn';
$str = str_replace( 'Freetuts', 'Freetuts.net', $str );
echo $str; // kết quả là Freetuts.net Xin Chào Các Bạn
```
```
$str = 'Freetuts Xin Chào Các Bạn';
$str = str_replace( array('Freetuts', 'Xin Chào'), array('Freetuts.net', 'Hello'), $str );
echo $str; // kết quả là Freetuts.net Hello Các Bạn
```
* md5($str) . Mã hóa chuỗi theo chuẩn md5 gồm 32 ký tụ
```
echo md5('pham van dat');
// Kết quả:d33e45112b24f3062737ef5116092e0a
```
* sha1($string) . Mã hóa chuỗi theo chuẩn sha1 gồm 40 ký tự
```
echo sha1('pham van dat');
// Kết quả:d6bc87d5ee95a511d83873ad24113c8c3460febf
```
* htmlentities($str) . Chuyển thể HTML sang dạng thực thể của cúng
```
echo htmlentities('<b>freetuts.net</b>');
// Kết quả <b>freetuts.net</b>
```
* html_entity_decode($string) . Chuyển các ký tự thực dngj sang HTML
```
$str = htmlentities('<b>freetuts.net</b>');
  
echo 'Entity: ' . $str . '<br/>';
echo 'Decode: ' . html_entity_decode($str);
// kế quả: Entity: <b>freetuts.net</b>
           Decode: freetuts.net
```
* strip_tags( $string, $allow_tags ) .  Bỏ các thẻ html trong chuỗi $string được khai báo ở $allow_tags
```
echo strip_tags('<b>freetuts.net</b>', 'b');

```
* echo strip_tags('<b>freetuts.net</b>', 'b'); . Lấy một chuỗi con nằm trong chuỗi $str bắt đầu từ ký tự thứ $start và chiều dài $length.
```
echo substr( 'freetuts.net',  0, 8);
// Kết quả freetuts
```
* strstr( $string, $ky_tu_cho_truoc ) . Tách một chuỗi bắt đầu từ  $ky_tu_cho_truoc cho đến hết chuỗi.
```
echo strstr('freetuts.net Xin Chào', 'Xin');
// Kết quả: Xin Chào
```
* strpos($str, $chuoi_tim ) . tìm vị trí của chuỗi $chuoi_tim trong chuỗi $str, kết quả trả về false nếu không tìm thấy.
```
echo strpos('freetuts.net chào các bạn', 'chào');
// kết quả 13
```

<a name="30"></a>
## 30. Giải thuật đệ quy trong php
**Đệ quy tuyến tính.**
 * Là dạng chỉ gọi duy nhất một lần đến chính nó trong hàm.
 * VD: Tính tổng các số nguyên từ 1 đến 10.
```
function tong($n)
{
     if($n=1)
         return = 1;
     return $n + tong($n-1);
}
```

<img src="http://imageshack.com/a/img922/7403/N9Z1dL.png">
 Với cách giải này khi n=1 thì xuất ra kết quả luôn hay còn là điều kiện để vòng lặp của đệ quy dừng. Biến n chạy từ n xuống tới 1 thì sẽ dừng lại và trả về kết quả tổng. Trong quá trình chạy xuống 1 đó nó đươc cộng dồn những số mà nó đã chạy qua. </br>
 Ta tưởng tương nếu n=10. thì đệ quy sẽ chạy như sau. 10 + (10-1=9) + (9-1=8) + ...... + (2-1=1) + 1; 

**Đệ quy nhị phân.**
 * Là hầm gọi về chính nó 2 lần.   
 * Vd: Bài toán thể hiện rõ nhất về dạng đẹ quy này là bài toán về dãy fibonacci. Dãy fibonacci là dãy bắt đầu từ 2 số 0 và 1 hoăc 1 và 1 mà số tiếp theo bằng tỏng 2 số kế trước nó.
```
function fibonacci($n)
{
     if ($n==1 || $n==2)
         return 1;
     return fibonacci($n-2) + fibonacci($n-1);
}
``` 

<img src="http://imageshack.com/a/img922/4991/zSJSjq.png">

**Đệ quy phi tuyến.**
 * Là đệ quy mà tỏng hàm có vòng lặp gọi lại chính nó.
 * Vd:
```
function day($n)
{
    if ($n<6)
        return $n;
    else
    {
        $tong=0;
        for($i=1;$i<$n;$i++)
        {
            $tong = $tong + day($n-$i);
        }
        return $tong;
    }
}
```

<img src="http://imageshack.com/a/img923/7245/3UpCzO.png">

**Đệ quy hỗ tương.**
 * Là đệ quy mà có 2 hàm gọi tới nhau. Ví dụ như hàm A gọi tới hàm B và hàm B lại gọi tới hàm A.
 * Vd:
<img src="http://imageshack.com/a/img923/4646/MMz5HK.png">

<a name="31"></a>
## 31. Các hàm xử lý mảng trong php
**Mở file**
 * Cú pháp mở file `open($path,$option)`
     * `$path` là đường dẫn đến file cần mở.
     * `$option` là quyền cho phép thao tác trên file
 * Danh sách các quyền.

| Moden | Diễn giả |
|-------|----------|
| r | Read only(chỉ đọc) |
| r+ | Read + Write(Đọc và viết) |
| w | Write only(chỉ viết) |
| w+1 | Write + Read. Xóa nội dung cũ của file và ghi nội dung mới cho file. Nếu trường hợp chưa có file thi file mới sẽ được tạo. |
| a | Mở file dưới dạng append(kết nối) dữ kiệu, chỉ có thể viết nếu file tồn tại thì ghi tiếp nội dung, còn không có file thì file mới xẽ được tạo ra. |
| a+ | Mở file dưới dạng append(kết nối) dữ liệu, Bao gồm viết và đọc file. Nếu file đã tồn tịa thì ghi tiếp vào file, còn chưa có file thì file mới sẽ được tạo ra. | 
| b | Mở dưới dạng binary(nhị phân) |
```
 $path = 'abc.txt'; //có thể tương đối hoạc tuyệt đối.
 $fp = @fopen($path, "r") // dù dấu @ để đề phòng trường hợp đường dẫ $path ta chuyền sai thì nó sẽ không bung lỗi ra màn hình.
 if (!$fp) 
 {
    echo 'Mở file không thành công';
 }
 else
 {
    echo 'Mở file thành công';
 }
```
<img src = "http://imageshack.com/a/img923/1415/M7Um6p.png">
<img src =" http://imageshack.com/a/img924/3954/y4x2si.png">

**Đọc file**
 * Có 3 cách đọc file:
     * Đọc từng ký tự ta dùng hàn `fgetc($fp)` 
     * Đọc theo từng dòng ta dùng hàm `fgets($fp)` </br>
     ***Đối với hai cách đọc này thì ta dùng hàm `feof($fp)` được đặt trong vòng lặp While để sau khi đọc song dòng hay song ký tự thì chuyển sang dòng hay ký tự mới.***
     * Đọc hết file ta dùng hàm `fread($fp, $size)`. Trong đó $fp là đối tượng mở file, $size kích cỡ file cần đọc. Dùng hàm filesize($path) để tính size của file.
 * **Ví dụ**
 * Đọc từng ký tự
<img src="http://imageshack.com/a/img924/5418/sqbcfN.png">
* Đọc từng dòng
<img src="http://imageshack.com/a/img922/4829/IeMVKM.png">
* Đọc cả file
<img src="http://imageshack.com/a/img923/1153/aXxVZ5.png">

**Ghi file** 
 * Để ghi file ta dùng hàm `fwrite($fp, $content)` trong đó `$fp` là đối tượng file càn ghi, `$content` là nội dung cần ghi(được nằm trong file đó).
 * Ví dụ
     * Ta dùng thuộc tính **w**
<img src="http://imageshack.com/a/img923/425/G728C5.png">

* Ta dùng thuộc tính **a** và file `dat.txt` đã có sẵn.

<img src="http://imageshack.com/a/img923/4012/IrqluO.png">

* Ta dùng thuộc tính **a** và file `abc.txt` chưa có trong thư mục. Ta chứ ý tới số lần nhấp vào tải lại trang. Nhấp bao nhiêu lần thì file của chúng ta sẽ được tạo thêm dữ liệu chuyền vào bấy nhiêu lần.

<img src="http://imageshack.com/a/img922/4929/SoqYXR.png">
<img src="http://imageshack.com/a/img922/3862/TmJp3Z.png">
<img src="http://imageshack.com/a/img924/198/uInwd4.png">







<a name="32"></a>
## 32. Các hàm xử lý file trong php

<a name="33"></a>
## 33. Expression matching

<a name="34"></a>
## 34. Upload file lên server với php

<a name="35"></a>
## 35. Các hàm kiểm tra dữ liệu trong php

<a name="36"></a>
## 36. Session và cookie trong php

<a name="37"></a>
## 37. Hàm isset() và empty() trong php

<a name="38"></a>
## 38. Xử lý truy vấn dữ liệu MySQL với PHP

<a name="39"></a>
## 39. Lệnh require - require_once - include - include_once trong PHP

<a name="40"></a>
## 40. Xử lý ngày tháng trong PHP

<a name="41"></a>
## 41. Các hàm xử lý mảng trong php

<a name="42"></a>
## 42. Tìm hiểu hàm header trong PHP

<a name="43"></a>
## 43. PHP Filter - Hàm filter_var trong PHP

<a name="44"></a>
## 44. Header Request và Header Response

## Hoàn thành Task.