# ALICE-Climate SaaS

Planetary climate simulation API with SDF atmospheric fields

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Climate |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/simulate` | 気候シミュレーション実行 |
| `GET  /api/v1/fields` | 大気フィールドデータ取得 |
| `POST /api/v1/forecast` | 気候予測 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
