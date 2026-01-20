- Người thực hiện : Lê Nguyễn Thanh Phúc
- Mã sinh viên : bit230325


### Kết quả thực hành tuần 1_trải nghiệm chất lượng giao diện phần mềm với https://cantunsee.space/ 
![Kết quả Can't Unsee](src/image/ketqua_cantunsee_1.png)

### Kết quả thực hành tuần 2
Dự án Student Grade Analysis là bài thực hành kiểm thử đơn vị (Unit Testing) nhằm áp dụng JUnit 5 để kiểm tra tính đúng đắn của các phương thức xử lý điểm số học sinh được viết bằng Java.
-Dự án thực hành kiểm thử đơn vị (Unit Testing) cho hệ thống phân tích điểm số học sinh sử dụng Java và JUnit 5.

Mô tả dự án
Chương trình cung cấp lớp `StudentAnalyzer` để phân tích danh sách điểm số của học sinh với các quy tắc sau:

- countExcellentStudents
  - Đếm số học sinh đạt loại Giỏi
  - Điều kiện: điểm ≥ 8.0

- calculateValidAverage
  - Tính điểm trung bình của các điểm hợp lệ

- Validation
  - Chỉ chấp nhận điểm trong khoảng 0 – 10
  - Bỏ qua các giá trị nhỏ hơn 0 hoặc lớn hơn 10
  - Nếu danh sách rỗng, trả về kết quả mặc định là 0

Công nghệ sử dụng
-Ngôn ngữ: Java 17.
-Framework kiểm thử: JUnit 5 (Jupiter).
-Công cụ quản lý dự án: Maven.
-Hỗ trợ: AI Generative (Thought Partner) trong quá trình lập trình và thiết kế ca kiểm thử.

Kết quả :
![Kết quả Can't Unsee](src/image/ketqua_bai2.png)

### Kết quả thực hành tuần 3

### 1. Thông tin chung

* **Môn học:** Kiểm thử phần mềm
* **Bài thực hành:** Kiểm thử tự động End-to-End với Cypress
* **Công cụ sử dụng:**

    * Node.js
    * Cypress
    * IntelliJ IDEA Community
* **Website kiểm thử:** [https://www.saucedemo.com](https://www.saucedemo.com)


### 2. Môi trường và công cụ

* **Hệ điều hành:** Windows
* **Node.js:** Phiên bản 14 trở lên
* **IDE:** IntelliJ IDEA Community
* **Framework kiểm thử:** Cypress


### 3. Cấu trúc thư mục dự án

```
cypress-exercise/
 ├── cypress/
 │   └── e2e/
 │       ├── login_spec.cy.js
 │       └── cart_spec.cy.js
 ├── node_modules/
 ├── cypress.config.js
 ├── package.json
 └── package-lock.json
```
### 4. Code
Kiểm thử xóa sản phẩm khỏi giỏ hàng:

it('Should remove product from the cart', () => {
cy.get('.inventory_item').first().find('.btn_inventory').click();
cy.get('.shopping_cart_badge').should('have.text', '1');

// Remove
cy.get('.inventory_item').first().find('.btn_inventory').click();

cy.get('.shopping_cart_badge').should('not.exist');
});

Kiểm thử quy trình thanh toán:

it('Should complete checkout step one successfully', () => {
cy.get('.inventory_item').first().find('.btn_inventory').click();
cy.get('.shopping_cart_link').click();
cy.get('#checkout').click();

cy.get('#first-name').type('John');
cy.get('#last-name').type('Doe');
cy.get('#postal-code').type('12345');

cy.get('#continue').click();
cy.url().should('include', '/checkout-step-two.html');
});


### 5. Kết quả thực hiện

* Tất cả các kịch bản kiểm thử đều **chạy thành công (PASS)**.
* Các chức năng chính của hệ thống hoạt động đúng theo yêu cầu.

![Kết quả Can't Unsee](src/image/ketqua_bai3_2.png)
![Kết quả Can't Unsee](src/image/ketqua_bai3_3.png)
![Kết quả Can't Unsee](src/image/ketqua_bai3_1.png)