# Consumer–Provider Handshake

## Thông tin chung

- Lab: FIT4110 Lab 03
- Ngày: 21/05/2026
- Provider team: team-vision
- Consumer team: team-iot
- Provider service: AI Vision Service
- Consumer service: IoT Ingestion Service

## Contract

- Contract file: contracts/ai-vision.openapi.yaml
- Mock base URL: http://localhost:4011
- Auth method: Bearer Token
- Endpoint được test: POST /detect

## Smoke test

### Request

```http
POST /detect
Authorization: Bearer lab-token
Content-Type: application/json

{
	"camera_id": "CAM01",
	"image_url": "https://example.com/frame.jpg"
}
```

### Response (mẫu)

```json
{
	"detection_id": "DET001",
	"label": "person",
	"confidence": 0.91,
	"risk_level": "medium"
}
```

### Kết quả

- [x] Gửi request thành công, nhận status 200.
- [x] Đọc được các field: detection_id, label, confidence.
- [ ] Không có lỗi 4xx/5xx.
- [x] Đã lưu evidence (Newman report/ảnh chụp).

## Xác nhận

- Đại diện provider: 
- Đại diện consumer: 

```json
{
}
```

### Expected response

```json
{
}
```

## Kết quả

- [ ] Consumer gọi mock thành công.
- [ ] Consumer parse được field cần dùng.
- [ ] Consumer hiểu lỗi 4xx/5xx provider trả về.
- [x] Có Newman report hoặc screenshot.

## Ghi chú thay đổi hợp đồng

| Nội dung | Trước | Sau | Người đồng ý |
|---|---|---|---|
| | | | |

## Xác nhận

- Provider representative:
- Consumer representative:
