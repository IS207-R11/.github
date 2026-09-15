# Thông tin nhóm

**Tên nhóm**: 200 OK.

**Danh sách thành viên**:

| STT | MSSV     | Họ và tên           | Vai trò     |
| --- | -------- | ------------------- | ----------- |
| 1   | 24520145 | Cao Thái Bảo        | Nhóm trưởng |
| 2   | 24520137 | Vũ Lê Minh Anh      | Thành viên  |
| 3   | 24521459 | Võ Minh Quân        | Thành viên  |
| 4   | 24521808 | Bùi Phan Giáng Trân | Thành viên  |

Trong trường hợp nhóm trưởng vì lý do cá nhân mà tạm thời không điều phối được công việc nhóm, nhóm trưởng phải chỉ định 1 thành viên làm nhóm trưởng tạm thời. Sự thay đổi này phải được ghi nhận lại tại danh sách thành viên này.

# Quy trình làm việc nhóm

### Yêu cầu

- **Minh bạch**: Mỗi task đều phải được giao qua _Github Project_, thành viên không được tự ý làm task không phải của mình hoặc không có trên _Github Project_.
- **Thái độ:** Thân thiện, hòa đồng, tích cực đóng góp vào dự án.
- **Tôn trọng ý kiến lẫn nhau:** Mọi quyết định đều phải thông qua bầu cử / bình chọn.
- **Công bằng:** Phân công công việc đều phải dựa trên năng lực và sở trường của mỗi thành viên.

### Công cụ quản lý dự án nhóm

Nhóm sử dụng _Github Organization_ và _Github Project_ để quản lý dự án.

#### Các liên kết truy cập nhanh

- [Project Hub](https://github.com/IS207-R11/.github): Chứa các tài liệu liên quan đến nhóm, quy trình làm việc và các tài liệu không phải mã nguồn.
- [Google Drive - Non-code repository](https://drive.google.com/drive/folders/1ajMGAQ2yEMmVwscEd1HeISssLvDxkZzC?usp=sharing): Lưu trữ các tài liệu báo cáo đồ án, log,...
- [Github Projects](https://github.com/orgs/IS207-R11/projects/1): Github Projects.
- [Main Project](https://github.com/IS207-R11/main-project): Mã nguồn main project.
- [Mini Project](https://github.com/IS207-R11/mini-project): Mã nguồn mini project.
- [Github Releases](https://github.com/IS207-R11/.github/releases): Lịch sử buổi họp.

#### Công cụ lập trình được khuyến khích sử dụng

- **IDE:** VS Code / Antigravity IDE.
- **Extension:** Git graph.

### Quy trình làm việc nhóm

#### Đối với các task về lập trình

1. Nhóm trưởng giao task (issue) cho các thành viên tại _Github Projects_ với trạng thái _In Progress_.
2. Tại máy tính của mình, thành viên tạo một nhánh mới từ nhánh `main` với tên `task/<task number>`. Mọi thay đổi của task đều chỉ được thực hiện tại nhánh đó.
3. Sau khi hoàn thành task, thành viên tạo một _Pull Request_ (PR) để merge vào nhánh `release/<sprint number>`, assign nhóm trưởng vào review.
4. Nhóm trưởng sẽ review PR:
   1. Nếu PR bị conflicts hoặc fail CI, thành viên cần chủ động tạo thêm commit để resolve.
   2. Nếu PR pass CI và is able to merge, nhóm trưởng sẽ merge PR, thành viên chuyển trạng thái task là _In Release_.

Mỗi task lớn phải bao gồm nội dung, trạng thái, người thực hiện và người review (khi PR). Thành viên thực hiện task cần tự ước lượng thời gian hoàn thành dựa trên năng lực và thời gian biểu của mình.

Thành viên có thể chủ động tạo subtasks để dễ quản lý.

> [!important]
>
> - Mỗi task chỉ được thực hiện bằng 1 nhánh duy nhất. Trong các trường hợp đặc biệt, thành viên cần thông báo cho nhóm trưởng biết và quyết định.
> - Thành viên không được phép merge nhánh vào `release/<sprint number>` hoặc `main`. Toàn bộ đều phải thông qua PR.
> - Chỉ có nhóm trưởng mới có quyền merge nhánh `release/<sprint number>` vào `main`.
> - Mỗi repository có `README.md` và tài liệu riêng.

> [!tip]
> Nếu nhánh bị conflict, thành viên có thể giải quyết bằng cách merge nhánh `relase/<sprint number>` ngược vào nhánh của mình, sau đó resolve conflicts tại máy tính của mình.

Mỗi sprint có thời hạn là **1 tuần** (trong các trường hợp đặc biệt có thể gia giảm).

**Cuối mỗi tuần:**

1. Các thành viên pull `release/<sprint number>` về máy, chạy local để kiểm tra tính năng mình làm có đúng chưa, có thiếu/mất code không.
1. Nhóm trưởng tạo meeting vào **8h tối thứ 7** cho các thành viên demo kết quả đạt được _(có ghi hình lại để tiện báo cáo cho thầy)_.
1. Nếu task đã đạt:
   1. Nhóm trưởng thay đổi trạng thái task thành _In Production_.
   2. Nhóm trưởng deploy.
   3. Nhóm trưởng tạo [Github Releases](https://github.com/IS207-R11/.github/releases) ghi nhận lại kết quả trong sprint vừa qua.
   4. Nhóm trưởng merge nhánh `release/<sprint number>` vào `main` và deploy `main`.
1. Nhóm trưởng tạo các task mới cho các task chưa đạt và cho milestones chung.

**Bảng tóm tắt các trạng thái của task**:
| Trạng thái | Ý nghĩa |
|-------------------|-------------------------------------------------------------------------|
| **In Progress** | Task đã bàn giao. |
| **In Release** | Task đã code xong (chưa demo nghiệm thu) và đã merge vào nhánh release. |
| **In Production** | Task đã hoàn thành và đã merge vào nhánh main. |
| **Canceled** | Task bị hủy. |

**Một số lệnh hữu ích khi lập trình**:
```sh
# --- Khi mới bắt đầu nhận task : Tạo nhánh mới có tên task/<task number> ---
git checkout -b task/<task number>

# --- Khi bắt đầu code : Cập nhật nhánh ---
git pull origin main

# --- Trong khi code : Lưu code và đưa lên Github
git add .
git commit -m "<Mô tả ngắn gọn code của bạn bằng tiếng Anh hoặc tiếng Việt>"
git push -u origin main

# --- Sau khi hoàn thành task : Mở Github lên và tạo Pull Request để merge vào nhánh release/<sprint number> (nếu không có release/<sprint number> thì nhắc nhóm trưởng tạo)
```

#### Đối với các task khác

Thành viên thực hiện trong các file tại repository này, không có quy định gì thêm.

### Quy trình CI

Code sẽ được kiểm tra qua các lệnh sau:

**Đối với _mini-project_**:

- **`npm ci`**: Kiểm tra xem project có thể cài đặt dependency thành công hay không.
- **`npm run lint`**: Kiểm tra xem project có vi phạm linting rules hay không (Static Analysis).
- **`npm run build`**: Kiểm tra xem project có thể build thành công hay không.
- Kiểm tra sự tồn tại của các file nhạy cảm (_.env_,...).

**Đối với _main-project_**: _Chưa xác định công nghệ, khi xác định rồi sẽ bổ sung sau_.

Khi thành viên tạo PR, _Github Actions_ sẽ tự động kiểm tra mã bằng các lệnh trên. Nếu CI fail, PR sẽ bị block.

Thành viên có thể chủ động kiểm tra tại thiết bị của mình trước khi PR.

### Quy trình CD

Chỉ áp dụng với _mini-project_.

Khi nhóm trưởng push `main`, _Github Actions_ sẽ tự động deploy bằng Vercel. Nếu deploy fail, nhóm trưởng sẽ:

1. Tạo issue mới và giao cho thành viên liên quan resolve vấn đề hoặc nhóm trưởng sẽ tự resolve.
2. Sau khi resolve, nhóm trưởng push lại `release/<sprint number>` và merge vào `main`.
