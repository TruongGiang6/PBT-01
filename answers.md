## PHẦN A:

## Câu A1:

1. Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, 5 bước xảy ra là:
- B1: Gửi Request qua hạ tầng mạng (DNS Lookup)
- B2: Server tiếp nhận và xử lý
- B3: Trả về Response
- B4: Phân tích cấu trúc (Parse HTML & CSS)
- B5: Thực thi và hiển thị (Execute JS & Render)
(Cuộc Hành Trình 0.3 Giây Xuyên Đại Dương/ Browser Rendering — Từ Code thành Hình ảnh)
2. Trong DevTools của Chrome, tab Network cho thấy các yêu cầu (requests) và phản hồi (responses) giữa trình duyệt và máy chủ

## Câu A2:

- Trang web bị Google đánh giá SEO thấp vì trang web trên mắc lỗi "Div Soup". Google và các công cụ tìm kiếm sử dụng các robot crawler để đọc mã nguồn, khi dùng <div> cho mọi thứ, robot không thể phân biệt được đâu là phần đầu, đâu là nội dung chính, hay đâu là một sản phẩm cụ thể. ("Dùng đúng thẻ = Google hiểu nội dung = SEO tốt hơn." > ❌ "Div Soup" — Google không hiểu gì.")

- 4 lỗi semantic: 
1. <div class="header"> -> <header>
2. <div class="menu"> -> <nav>
3. <div class="main"> -> <main>
4. <div class="product"> -> <article>

- Code sửa:
<header>
    <div class="logo">ShopTLU</div>
    <nav>
        <div><a href="/">Trang chủ</a></div>
        <div><a href="/products">Sản phẩm</a></div>
    </nav>
</header>
<main>
    <article>
        <div class="title">iPhone 16 Pro</div>
        <div class="price">25.990.000đ</div>
        <div class="image"><img src="iphone.jpg"></div>
    </article>
</main>
<div class="footer">© 2026 ShopTLU</div>

## Câu A3:

- Text Art: 
 Hộp 1                                             
 Text AText B                                      
 Hộp 2                                             
 Text CText D                                      
 Hộp 3

- Giải thích:
+<div>Hộp 1</div>,<div>Hộp 2</div>,<div>Hộp 1</div>: Là 1 block, chiếm riêng 1 dòng
+<span>Text A</span> <span>Text B</span>, <span>Text C</span> <strong>Text D</strong>: là inline, nằm cạnh nhau 

## Câu A4:

*** Sự khác nhau giữa <thead>, <tbody>, <tfoot> ***:
- <thead> (Table Header): chứa các tiêu đề của cột (thường dùng kết hợp với thẻ <th>)
- <tbody> (Table Body): chứa nội dung dữ liệu chính của bảng
- <tfoot> (Table Footer): chứa thông tin tổng kết hoặc chú thích cuối bảng
*** KHÔNG NÊN dùng table để tạo layout trang web vì ***:
1. Sai mục đích Semantic: nếu dùng để chia bố cục trang web (header, sidebar, footer), các công cụ tìm kiếm sẽ không hiểu được đâu là nội dung chính, dẫn đến SEO cực kỳ kém
2. Không linh hoạt: bảng có cấu trúc rất cứng nhắc. Khi xem trên điện thoại di động (màn hình nhỏ), một layout bằng table sẽ bị vỡ vụn hoặc bị tràn màn hình, rất khó để thu gọn hay sắp xếp lại
3. Tốc độ tải trang chậm: trình duyệt thường phải đợi tải xong toàn bộ code của thẻ <table> thì mới bắt đầu tính toán để hiển thị ra màn hình. Nếu layout trang web phức tạp với nhiều bảng lồng nhau, người dùng sẽ thấy một trang trắng tinh trong thời gian dài trước khi nội dung hiện ra
