**Khái niệm cốt lõi của if/else**

**if/else = ra quyết định.** Máy tính kiểm tra một điều kiện (đúng/sai), rồi chọn nhánh thực thi tương ứng.
```
if (điều kiện đúng) {

làm việc A

} else {

làm việc B

}
```

Ba dạng cơ bản:

-   **if đơn:** chỉ làm gì đó khi điều kiện đúng, sai thì bỏ qua.
-   **if/else:** đúng làm A, sai làm B (luôn chạy một trong hai).
-   **if/else if/else:** nhiều điều kiện xếp tầng, kiểm tra lần lượt từ trên xuống, gặp cái đúng đầu tiên thì dừng.

----------

**Cách rèn tư duy phân loại điều kiện**

**1. Liệt kê hết các trường hợp (case) trước khi viết code.**  
Tự hỏi: "Có bao nhiêu khả năng xảy ra?" Ví dụ phân loại điểm: giỏi / khá / trung bình / yếu → 4 nhánh.

**2. Đảm bảo các nhánh bao phủ hết (MECE).**  
Hai nguyên tắc:

-   _Không bỏ sót:_ mọi giá trị đầu vào phải rơi vào đúng một nhánh.
-   _Không chồng chéo:_ một giá trị không được khớp hai nhánh cùng lúc.
```
if (điểm >= 8)  → giỏi

else if (điểm >= 6.5) → khá  // tự động hiểu là 6.5–7.9

else if (điểm >= 5)  → trung bình

else  → yếu  // bắt mọi trường hợp còn lại
```
Để ý: nhờ else if xếp tầng nên không cần viết điểm >= 6.5 && điểm < 8. Thứ tự quan trọng — kiểm tra từ mốc cao xuống thấp.

**3. Luôn xử lý biên (boundary) và trường hợp đặc biệt.**  
Dấu >= hay >? Giá trị bằng đúng mốc thuộc nhánh nào? Đầu vào âm, bằng 0, rỗng, null thì sao? Lỗi if/else thường nằm ở ranh giới.

**4. Dùng else cuối làm "lưới an toàn".**  
Nhánh else cuối bắt mọi thứ chưa được liệt kê, tránh để chương trình rơi vào trạng thái không xác định.

**5. Bài tập rèn luyện cụ thể.**

-   Kiểm tra số chẵn/lẻ.
-   Phân loại tam giác (đều / cân / vuông / thường) — buộc bạn nghĩ về điều kiện kết hợp.
-   Tính tiền điện theo bậc thang — luyện điều kiện xếp tầng.
-   Kiểm tra năm nhuận — luyện điều kiện lồng nhau và toán tử logic.

**Mẹo tư duy:** trước khi code, viết ra giấy dạng bảng "Nếu... thì...". Khi bảng đầy đủ và không mâu thuẫn, dịch sang if/else gần như cơ học.

