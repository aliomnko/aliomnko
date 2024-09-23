# V2Ray Server on Vercel

این پروژه یک سرور V2Ray است که در Vercel مستقر شده است.

## توضیحات

این سرور از پروتکل VLESS استفاده می‌کند و برای کاربرانی که به دنبال یک راه‌حل VPN سریع و امن هستند، طراحی شده است.

## پیکربندی

فایل پیکربندی `config.json` شامل تنظیمات سرور است. لطفاً قبل از استفاده، UUID خود را در این فایل جایگزین کنید:

```json
{
  "inbounds": [
    {
      "port": 10086,
      "protocol": "vless",
      "settings": {
        "clients": [
          {
            "id": "Abol", // جایگزین کنید
            "alterId": 0
          }
        ]
      }
    }
  ],
  "outbounds": [
    {
      "protocol": "freedom",
      "settings": {}
    }
  ]
}
