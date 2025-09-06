# Bài 1
Ta có **N** cột đá hình hộp chữ nhật liên tiếp và sát nhau có độ cao lần lượt là `h₁, h₂, ..., hₙ`.  

Ta thấy rằng các cột đá có thể chứa được nước. Giả sử `N = 7`, với các độ cao `hᵢ` lần lượt là: 2 5 1 3 4 3 6 thì ta chứa được lượng nước bằng **9** 

---

Mục tiêu là chứa nhiều nước nhất có thể. Tuy nhiên, do kinh phí có hạn, ta chỉ có thể **tăng thêm 1 đơn vị chiều cao cho nhiều nhất một cột đá bất kỳ**.  

Hãy giúp tính lượng nước tối đa có thể chứa được.

---

### Input
- Dòng đầu tiên chứa một số nguyên dương duy nhất `N` (`N ≤ 10⁶`).
- Dòng thứ hai chứa `N` số nguyên dương, số thứ `i` là độ cao `hᵢ` của cột đá thứ `i` ban đầu (`hᵢ ≤ 10⁹`).

---

### Output
- In ra số nguyên duy nhất là kết quả của bài toán.

---

### Ví dụ

#### Sample Input
7

2 5 1 3 4 3 6
#### Sample Output
13

---

### Giới hạn chấm điểm
- **Subtask 1** (40% số test): `1 ≤ N ≤ 10³`.
- **Subtask 2** (60% số test): Không có ràng buộc gì thêm.

# Bài 2
Bạn được cho một mảng gồm **N** số nguyên `A`, được đánh chỉ số từ `0` đến `N-1`. Có tất cả `Q` truy vấn cần xử lý.  

Mỗi truy vấn được mô tả bởi cặp chỉ số `(l, r)` và yêu cầu bạn xác định:  
> Độ dài lớn nhất của một **đoạn con liên tiếp** nằm hoàn toàn trong phạm vi `[l, r]` sao cho trong đoạn con này **không có hai phần tử nào trùng giá trị**.

---


### Input
- Dòng đầu tiên: chứa hai số nguyên `N, Q` (`N, Q ≤ 10⁵`).
- Dòng thứ hai: gồm `N` số nguyên (|Aᵢ| ≤ 10¹⁸).
- `Q` dòng tiếp theo: mỗi dòng gồm 2 số `l, r` (`0 ≤ l ≤ r < N`) tương ứng với một truy vấn.

---

### Output
- Gồm `Q` dòng, mỗi dòng là câu trả lời cho một truy vấn.

---

### Ví dụ

#### Sample Input
9 2

0 3 2 -1 0 1 4 0 2

0 8

2 6

#### Sample Output
6

5

# Bài 3

Alice vừa đoạt giải quán quân trong một kỳ thi lập trình danh giá. Ban tổ chức trao thưởng thông qua một trò chơi như sau.  
Có `n` thẻ xếp trên một hàng dài, trên mỗi thẻ viết một số nguyên dương.  
Ban tổ chức cho phép Alice thực hiện nhiều bước để chọn ra đúng `k` cặp thẻ, mỗi bước thực hiện theo một trong các quy tắc sau:

1. Chọn 2 thẻ đầu hàng;  
2. Chọn 2 thẻ cuối hàng;  
3. Chọn 1 thẻ đầu hàng và 1 thẻ cuối hàng;  
4. Loại 1 thẻ đầu hàng ra khỏi hàng;  
5. Loại 1 thẻ cuối hàng ra khỏi hàng.  

Sau mỗi bước nếu chọn được 2 thẻ thì loại 2 thẻ đó ra khỏi hàng và Alice nhận được số tiền thưởng bằng giá trị tuyệt đối của hiệu hai số ghi trên hai thẻ đó.  

---

### Yêu cầu
Hãy giúp tìm cách chơi chọn đúng `k` cặp thẻ để đạt được tổng số tiền thưởng là lớn nhất.

---

### Input
- Dòng thứ nhất chứa hai số nguyên dương `n` và `k` (`2 × k ≤ n`);  
- Dòng thứ hai chứa `n` số nguyên dương là giá trị ghi trên từng thẻ, mỗi thẻ một số tương ứng lần lượt từ đầu hàng.  
  Các số có giá trị không vượt quá `10^9`.

Các số trên cùng một dòng cách nhau bởi dấu cách.  

---

### Output
Ghi ra một số nguyên duy nhất là tổng tiền thưởng lớn nhất tìm được.

---

### Giới hạn
- Có 40% số test ứng với 40% số điểm của bài thỏa mãn điều kiện: `n ≤ 300, k ≤ 2`;  
- 40% số test khác ứng với 40% số điểm của bài thỏa mãn điều kiện: `n ≤ 30, 2 × k = n`;  
- 20% số test còn lại ứng với 20% số điểm của bài thỏa mãn điều kiện: `n ≤ 300`.  

---

### Sample Input
6 2

1 3 10 2 1 4

## Sample Output
12

---

## Note
**Giải thích test ví dụ**  

- Bước 1: Alice chọn hai thẻ cuối hàng là `1` và `4` và nhận được số tiền thưởng là `|4 − 1| = 3`;  
- Bước 2: Alice loại thẻ cuối hàng có giá trị `2`;  
- Bước 3: Alice chọn một thẻ đầu hàng và một thẻ cuối hàng là `1` và `10` và nhận được số tiền thưởng là `|10 − 1| = 9`;  

Tổng tiền thưởng Alice nhận được là `3 + 9 = 12`.  