# __Tìm hiểu về Markdown__
---
## __Markdown và lịch sử hình thành__

`Markdown` là một ngôn ngữ đánh dấu với cú pháp văn bản thô, được thiết kế để có thể dễ dàng chuyển thành `HTML` và nhiều định dạng khác sử dụng một công cụ cùng tên. Nó thường được dùng để tạo các tập tin `readme`, viết tin nhắn trên các diễn đàn, và tạo văn bản có định dạng bằng một trình biên tập văn bản thô

Năm 2004, cùng với sự giúp đỡ của __Aaron Swartz__, __John Gruber__ đã tạo ra ngôn ngữ `Markdown` với mục tiêu tạo ra một định dạng văn bản thô "dễ viết, dễ đọc, dễ dàng chuyển thành `XHTML` (hoặc `HTML`).

`Markdown` dùng các dấu hiệu từ các quy ước cho văn bản thô trong email, như setext - một ngôn ngữ được thiết kế để có thể đọc bình thường mà không phải lục lọi giữa các thẻ định dạng, khác với văn bản trong ngôn ngữ đánh dấu như RTF hay HTML, vốn chứa nhiều thẻ và cú pháp khó đọc. Gruber đã viết một công cụ nhỏ bằng Perl, `Markdown`.pl, cho phép chuyển đổi đoạn văn bản đã đánh dấu theo chuẩn `Markdown` sang XHTML hoặc HTML. Tiện ích này có thể dùng một mình, hoặc dùng như là plugin cho Bloxom hoặc Movable Type, hoặc là một bộ lọc cho BBEdit.

`Markdown` sau đó đã được hoàn thiện thành một module Perl và công bố trên CPAN (Text:: `Markdown`) cũng như trên một vài ngôn ngữ khác. Nó được phân phối theo giấy phép BSD và được nhúng sẵn, hoặc là plugin của một số hệ thống quản lý nội dung. Một số trang web như `GitHub`, `reddit`, `Diaspora`, `Stack Exchange`, `OpenStreetMap`, `SourceForge` cũng sử dụng.

## __Cú pháp cơ bản__

### 1. __Tiêu đề (Heading)__

 Sử dụng ký tự # để biểu diễn các thẻ tiêu đề từ h1 tới h6.
 
 __Example:__

 ```
 # Heading 1

 ## Heading 2
 ---
 ### Heading 3
 ---
 #### Heading 4
 ---
 ##### Heading 5
 ---
 ###### Heading 6
 ---
 ````
 # Heading 1

 ## Heading 2
 ---
 ### Heading 3
 ---
 #### Heading 4
 ---
 ##### Heading 5
 ---
 ###### Heading 6
 ---

 ### 2. __Kiểu chữ (Character styles)__

 * Tạo chữ đậm: 
 ```
 __đậm__, **đậm**
 ```
 __đậm__, **đậm**

 * Tạo chữ nghiêng:
 ```
 _nghiêng_, *nghiêng*
 ```
 _nghiêng_, *nghiêng*

 * Tạo chữ vừa đậm vừa nghiêng:
 ```
 ___đậm và nghiêng___, *__đậm và nghiêng__*
 ```
 ___đậm và nghiêng___, *__đậm và nghiêng__*
 * Tạo chữ gạch ngang
 ```
 ~~gạch ngang~~
```
~~gạch ngang~~
* Code Style:
``` 
`code style`
```
`code style`
* Quote block:
```
>Quote block
>>Quote block
>
>Quote block
```
>Quote block
>>Quote block
>
>Quote block

### 3. __Danh sách (List)__

Để dánh dấu 1 danh sách không có thứ tự (unorder list) chúng ta sử dụng dấu - hoặc + hoặc * trước mỗi dòng. Để đánh dấu một danh sách có thứ tự bạn sử dụng các số thay vì các dấu như ở trên.

```
- Text1
+ Text2
  * Text3

1. Text1
2. Text2
3. Text 3
```
- Text1
+ Text2
    * Text3

1. Text1
2. Text2
3. Text 3

### 4. __Liên kết (Link)__
Để tạo một liên kết nội tuyến, sử dụng một tập hợp các dấu ngoặc đơn ngay sau ngoặc vuông. Bên trong ngoặc đặt URL mà bạn muốn liên kết, cùng với một tiêu đề tùy chọn cho liên kết, bao bọc trong dấu ngoặc kép. Với URLs và URL đặt trong dấu ngoặc nhọn được chuyển thành liên kết trực tiếp

__Example :__
```
[Google](http://google.com.vn)

<http://Google.com.vn>

http://Google.com.vn
```
[Google](http://google.com.vn)

<http://Google.com.vn>

http://Google.com.vn

### 5. __Code và block__
Có 2 loại code có thể viết trong markdown: inline code (code trong dòng) và code block (đoạn code riêng). sử dụng lần lượt 1 ký tự và 3 ký tự `

__Example__:
```
Đây là ví dụ về inline code `inline code`

Còn đây là block code

```c++
class H1{
    private: 
        int a,b,c;
    public:
        void input();
        void ouput();
}
```/
``` 
__Kết quả:__

Đây là ví dụ về inline code `inline code`

Còn đây là block code

```c++
class H1{
    private: 
        int a,b,c;
    public:
        void input();
        void ouput();
}
``` 
### 6. __Dấu gạch ngang (Horizontal rule)__
Sử dụng 3 hoặc nhiều hơn dấu ___ hoặc *** hoặc --- để tạo dấu gạch ngang để được kết quả sau:

---
### 7. __Tạo đoạn văn bản trong Markdown__
Sử dụng phím `Enter` để tạo thêm 1 dòng trống giúp tạo ngăn cách giữa 2 đoạn văn bản giống như sau:

```
Task lists allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the content. To create a task list,
<Enter>
add dashes (-) and brackets with a space ([ ]) in front of task list items. To select a checkbox, add an x in between the brackets ([x]).
```

Task lists allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the content. To create a task list,

add dashes (-) and brackets with a space ([ ]) in front of task list items. To select a checkbox, add an x in between the brackets ([x]).

### 8. __Ảnh__
Hình ảnh trong Markdown tương tự như liên kết. Sự khác biệt là:
- Các dấu ngoặc vuông phải được bắt đầu bằng một dấu chấm than
- Và bên trong chúng có thể có một số văn bản thay thế. Mô tả về hình ảnh, nó sẽ được hiển thị nếu hình ảnh bị lỗi.
![sxr155](../image/sxr155.jpg)

### 9. __HTML nội tuyến__

Cú pháp HTML thô vẫn hoạt động khá tốt ở trong văn bản Markdown

__Example:__
```
<h1>Thẻ h1</h1>
<h2>Thẻ h2</h2>
<h3>Thẻ h3</h3>
```
<h1>Thẻ h1</h1>
<h2>Thẻ h2</h2>
<h3>Thẻ h3</h3>

---

Link tham khảo:

<https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#html>

<https://www.markdownguide.org/cheat-sheet>

<https://vi.wikipedia.org/wiki/Markdown>
