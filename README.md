# Front-end Developer Test - Angular (Retail App)

## 👋 Giới thiệu
Chào mừng bạn đến với bài test tuyển dụng vị trí **Lập trình viên Front-end (Angular)** tại KidsPlaza.  
Bài test này giúp chúng tôi đánh giá kỹ năng HTML, CSS, tư duy component hóa và kiến thức cơ bản về Angular, bao gồm cách bạn làm việc với **Routing**, **Observables**, và cấu trúc một dự án thực tế.

---

## 🎯 Yêu cầu chung

Hãy xây dựng một ứng dụng quản lý sản phẩm đơn giản trong lĩnh vực bán lẻ với các tính năng sau:

### 1. Trang danh sách sản phẩm `/products`
- Hiển thị danh sách sản phẩm dưới dạng thẻ (grid layout)
- Mỗi thẻ sản phẩm bao gồm:
  - Hình ảnh sản phẩm
  - Tên sản phẩm
  - Giá tiền (VNĐ)
  - Trạng thái còn hàng
  - Nút **Xem chi tiết**

### 2. Trang chi tiết sản phẩm `/products/:id`
- Hiển thị thông tin chi tiết của một sản phẩm khi người dùng nhấn nút "Xem chi tiết".
- Thông tin bao gồm:
  - Hình ảnh lớn
  - Tên sản phẩm
  - Mô tả
  - Giá
  - Trạng thái hàng
- Nút "Quay lại" để trở về danh sách

### 3. (Bonus) Tìm kiếm sản phẩm theo tên
- Thêm input tìm kiếm (search box)
- Kết quả hiển thị thay đổi theo từ khóa tìm kiếm (dùng `@Input`, `@Output`, `ngModel`, hoặc Reactive Forms)

---

## 🧠 Yêu cầu bắt buộc sử dụng `Observable`:

- **Yêu cầu thêm:**  
  Tạo một **ProductService** trả về danh sách sản phẩm thông qua `Observable<Product[]>` (không trả về trực tiếp `Array`).
  
- Gợi ý:  
  ```ts
  getProducts(): Observable<Product[]> {
    return of(PRODUCTS); // giả lập từ mock data
  }

  getProductById(id: number): Observable<Product | undefined> {
    return of(PRODUCTS.find(p => p.id === id));
  }

## 📦 Dữ liệu mẫu (mock)
- Tạo danh sách sản phẩm trong file .ts (không cần kết nối API). Ví dụ:
  ```ts
  export const PRODUCTS = [
  {
    id: 1,
    name: 'Áo thun cotton nam',
    image: 'https://via.placeholder.com/150',
    price: 199000,
    description: 'Chất liệu cotton mềm mịn, thoáng khí.',
    inStock: true
  },
  {
    id: 2,
    name: 'Quần jeans nữ',
    image: 'https://via.placeholder.com/150',
    price: 399000,
    description: 'Form dáng ôm nhẹ, hợp thời trang.',
    inStock: false
  },
  ...
];

## 🎨 Yêu cầu về giao diện
- Responsive đơn giản (hiển thị đẹp trên mobile và desktop)
- Ưu tiên viết CSS thủ công (không dùng Bootstrap hoặc Tailwind)
- Ưu tiên giao diện rõ ràng, dễ sử dụng

## 🛠 Yêu cầu kỹ thuật
- Angular 15+
- Không dùng external UI library (có thể dùng Angular Material nếu bạn thấy cần thiết, nhưng không bắt buộc)
- Không cần kết nối backend thật, chỉ dùng mock data nội bộ

## 📬 Gửi bài
Sau khi hoàn thành, bạn vui lòng gửi:
- Link GitHub (hoặc file zip)
- Hướng dẫn chạy (nếu cần)
- Ghi chú đặc biệt (nếu bạn muốn chia sẻ thêm về cách làm hoặc highlight phần nào đó bạn tự tin nhất!)



