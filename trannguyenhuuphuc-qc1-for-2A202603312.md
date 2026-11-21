# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): `2A202603312 - Vũ Văn Long` (file/manifest)        Người kiểm (học viên): `trannguyenhuuphuc`  
Ngày: 2026-11-20                          Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): `2A202603312.zip` (chỉ có 1 file front; thiếu `<tên>-fisheye.zip` và thiếu `<tên>-manifest.json`, chưa rõ `revision`)  
Số ảnh kiểm: 6 (`A01–A06` đã gán nhãn) (+ 6 ảnh `A07–A12` trong file chưa gán nhãn, kiểm bổ sung ở `QC1-12`)   Số nhãn đã kiểm (shape + tag): `81` (`57` shape + `24` tag trên `A01–A06`)

> Ảnh ghi nhận **không lỗi** về shape/nhãn chính để đối chiếu: `A06_b8c66e31-37045eec.jpg` (chỉ có một ca mơ hồ `lane#0` vạch đôi một liền một đứt QCVN 1.4 và tag `weather=clear` cần lead chốt thêm).

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 24 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 9 | 1 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 15 | 3 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 15 | 2 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 15 | 2 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 15 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 26 | 3 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 7 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 16 | 1 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 9 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 0 | 0 | chính |
| QC1-12 file | lỗi file | 81 | 8 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-02 | A03_b1c66a42-6f7d68ca.jpg | lane (thiếu L1) | nặng | Bỏ sót hoàn toàn vạch tim đường đôi màu vàng (`L1`) dọc mép trái làn xe đang đi (`drivable#3`). |
| 2 | QC1-03 | A01_bc5fadac-fa6dd225.jpg | lane#0@(695,710) | nặng | Vạch đứt trắng bên phải làn xe đang đi (`R1`) bị gán sai `position=L1`. |
| 3 | QC1-03 | A01_bc5fadac-fa6dd225.jpg | lane#3@(0,601) | nặng | Vạch mép đường bên trái (`L2`) bị gán sai `position=R2`. |
| 4 | QC1-03 | A01_bc5fadac-fa6dd225.jpg | lane#4@(1280,706) | nặng | Vạch mép đường ngoài cùng bên phải (`R2`) bị gán sai `position=L1`. |
| 5 | QC1-04 | A02_b3c26aff-63a0d7d6.jpg | lane#5@(530,416) | chính | Vẽ thêm polyline `L1` ngắn bị lệch hẳn khỏi tâm vạch sang làn bên trái (`(530,416)-(546,399)`). |
| 6 | QC1-04 | A04_b7a8e795-0ff55db2.jpg | lane (thiếu R2) | chính | Bỏ sót vạch đôi liền màu trắng (`R2`) ngăn làn xe đạp màu xanh ở góc phải ảnh. |
| 7 | QC1-05 | A02_b3c26aff-63a0d7d6.jpg | lane#6@(577,404) | chính | Tách đoạn xa của vạch đứt `L1` thành polyline riêng chồng gần chân trời và gán `style=solid`. |
| 8 | QC1-05 | A04_b7a8e795-0ff55db2.jpg | lane#1@(39,553), lane#2@(532,344) | chính | Vạch tim đường đôi vàng liên tục `L1` bị tách thành 2 polyline rời qua đoạn ngắt ngắn (cần nối liền 1 đường). |
| 9 | QC1-07 | A03_b1c66a42-6f7d68ca.jpg | drivable#4@(944,677) | chính | Vùng `drivable (alternative)` bên phải mở rộng tràn qua dải đỗ xe phía trước xe van trắng sát lề. |
| 10 | QC1-07 | A04_b7a8e795-0ff55db2.jpg | drivable#8@(730,537) | chính | Vùng `drivable (alternative)` tràn qua vạch đôi trắng sang cả làn xe đạp tô xanh lá ở mép phải. |
| 11 | QC1-07 | A05_b2576c8c-2de20b8a.jpg | drivable#1@(285,540) | chính | Vùng `drivable (direct)` vẽ quá hẹp, bỏ sót phần mặt đường nhựa rộng sát dãy xe đỗ bên trái và góc mở rộng bên phải. |
| 12 | QC1-09 | A03_b1c66a42-6f7d68ca.jpg | traffic_sign#7@(217,170) | chính | Biển quay lưng (`facing=back`) không thấy mặt biển nhưng vẫn đoán `group=prohibitory` (nên chọn `other` và ghi ca khó). |
| 13 | QC1-12 | toàn lô (`2A202603312.zip`) | file | nặng | Thiếu hoàn toàn file fisheye (`<tên>-fisheye.zip`); chỉ nộp 1 file zip cho ảnh front. |
| 14 | QC1-12 | toàn lô (`2A202603312.zip`) | file | nhẹ | Sai quy ước tên file (`2A202603312.zip` thay vì `<tên>-front.zip`) và thiếu `<tên>-manifest.json`. |
| 15 | QC1-12 | A07_b41ace08-c8468690.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |
| 16 | QC1-12 | A08_c0deebc1-16cfa791.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |
| 17 | QC1-12 | A09_c7e6d5d1-c8af9fe3.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |
| 18 | QC1-12 | A10_b6ff1331-f6d3fba8.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |
| 19 | QC1-12 | A11_c1f35f18-b529c043.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |
| 20 | QC1-12 | A12_c0f978fa-9b4e623f.jpg | image | nhẹ | Ảnh chưa có nhãn nào (`tags=0, shapes=0`). |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A06_b8c66e31-37045eec.jpg | `lane#0` là vạch đôi một liền một đứt (QCVN 1.4); bạn chọn `style=dashed` là hợp lệ theo guideline nhưng chưa ghi chú nửa đã chọn — có chấp nhận qua khi bổ sung ghi chú không? | |
| A04, A05, A06 | Bầu trời đều nhiều mây âm u (`overcast`) nhưng tag đang để `weather=clear` — có yêu cầu đổi đồng loạt sang `overcast` khi Rework không? | |
| A06_b8c66e31-37045eec.jpg | `traffic_light#14` (`pedestrian, facing=side`) để `color=off` trong khi `traffic_light#8` (`vehicle, facing=side`) để `color=unknown` — nên thống nhất theo `off` hay `unknown`? | |

## Quyết định
Lỗi nặng: 5   Lỗi chính: 8 / 81 nhãn = 9.9 %   Lỗi nhẹ: 7   Ca chờ lead: 3  
Quyết định (Release / Hold / Rework): **Rework**  
Lý do (theo luật của phiếu): Có **5 lỗi nặng** (`≥ 1` lỗi nặng → **Rework**, gồm `QC1-02` bỏ sót `L1` ở `A03`, 3 lỗi `QC1-03` sai `position` trên `A01`, và `QC1-12` thiếu file `<tên>-fisheye.zip`); đồng thời tỉ lệ lỗi chính đạt **8 / 81 nhãn = 9.9 %** (vượt ngưỡng 5 %), cộng thêm 6 ảnh bắt buộc (`A07–A12`) trong file front chưa được gán nhãn.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](docs/qc_severity_road_v1.0.md).
