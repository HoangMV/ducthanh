# Đức Thành - Hệ thống xác nhận đặt hàng

## Cài đặt

1. Clone repository về máy:
```bash
git clone <repository-url>
```

2. Tạo thư mục templates:
```bash
mkdir templates
```

3. Tạo file template Word:
- Tạo file `templates/order_template.docx` với nội dung sau:
```
CÔNG TY TNHH SẢN XUẤT VÀ DỊCH VỤ ĐỨC THÀNH

XÁC NHẬN ĐẶT HÀNG

Số đơn hàng: {order_number}
Ngày đặt hàng: {order_date}

THÔNG TIN KHÁCH HÀNG:
Khách hàng: {customer_name}
Mã số thuế: {tax_code}
Địa chỉ: {invoice_address}

THÔNG TIN GIAO HÀNG:
Người nhận: {recipient_name}
Điện thoại: {recipient_phone}
Địa chỉ giao hàng: {delivery_address}

DANH SÁCH SẢN PHẨM:
{#products}
STT: {stt}
Tên hàng hoá: {ten_hang_hoa}
Mô tả: {mo_ta}
Đơn vị tính: {dvt}
Số lượng: {so_luong}
Đơn giá: {don_gia}
Thành tiền: {thanh_tien}
----------------------------------------
{/products}

Cộng tiền hàng: {subtotal}
Thuế GTGT (8%): {tax_amount}
Tổng cộng: {grand_total}

{total_in_words}

          BÊN MUA                                    BÊN BÁN
        (Ký, họ tên)                              (Ký, họ tên)
```