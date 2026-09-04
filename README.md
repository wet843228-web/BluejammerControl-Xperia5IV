# BluejammerControl - Xperia 5 IV 専用版

ESP32-BlueJammer を Xperia 5 IV から WiFi 経由でリモート制御するアプリです。

## 📱 対応デバイス
- **Xperia 5 IV** (Android 14)
- 画面サイズ: 6.1 インチ
- 最適化: タッチ操作、バッテリー効率

## 🚀 機能（MVP版）
- [x] WiFi ネットワーク検出
- [x] ESP32 への自動接続
- [x] リモートコントロール（ON/OFF）
- [x] ステータス表示
- [x] リアルタイムフィードバック

## 📋 必要なもの
1. **ESP32 マイコンボード**
2. **ソフトバンク Air NEXT WiFi ネットワーク**
3. **Xperia 5 IV** (Android 14 以上)

## 🔧 セットアップ

### フェーズ 1: ESP32 ファームウェア構築
```bash
cd esp32_firmware
# Arduino IDE または platformio でアップロード
```

### フェーズ 2: Android アプリ構築
```bash
cd android_app
flutter pub get
flutter run
```

## 📡 通信プロトコル
- **Method**: HTTP REST API
- **Port**: 8080
- **Format**: JSON

### API エンドポイント
- `GET /api/status` - 現在の状態確認
- `POST /api/start` - 干扰開始
- `POST /api/stop` - 干扰停止
- `GET /api/config` - 設定取得

## ⚙️ ESP32 設定
```
SSID: [自動検出]
IP アドレス: 192.168.100.1 (ホットスポット)
ポート: 8080
```

## 📝 開発ロードマップ
- [ ] ファームウェア: WiFi サーバー実装
- [ ] アプリ: UI/UX 設計
- [ ] 通信: API テスト
- [ ] テスト: Xperia 5 IV で動作確認
- [ ] APK: ビルド & インストール

## 📄 ライセンス
Educational purposes only / 教育目的のみ

## ⚠️ 法的注意
このプロジェクトは教育・研究目的です。
違法な使用は禁止されています。
