# RKO — Kuran Okulu Kayıt Takip

Dönem bazlı kayıt takip dashboard'u.

## Canlı Site

- **Dashboard:** [https://www.rqsregistry.quranstudyportal.com/index.html](https://www.rqsregistry.quranstudyportal.com/index.html)
- **2026 Bahar:** [https://www.rqsregistry.quranstudyportal.com/2026-bahar/index.html](https://www.rqsregistry.quranstudyportal.com/2026-bahar/index.html)
- **2026 Yaz:** [https://www.rqsregistry.quranstudyportal.com/2026-yaz/index.html](https://www.rqsregistry.quranstudyportal.com/2026-yaz/index.html)
- **2026 Güz:** [https://www.rqsregistry.quranstudyportal.com/2026-guz/index.html](https://www.rqsregistry.quranstudyportal.com/2026-guz/index.html)

## Veri Şeması (`kayit.json`)

`teachers[]` alanları:

| Alan | Anlamı |
| --- | --- |
| `name` | Öğretmen adı |
| `arrived` | Kayıt döneminde gelen öğrenci |
| `total` | Toplam öğrenci |
| `ongoing` | Dersi hâlâ süren öğrenci — kayıt açamadığı için "gelmedi" sayılmaz |

`ongoing` barda gri dilim olarak gelenin yanına yığılır; sağdaki çatı yüzde
`(arrived + ongoing) / total` değeridir ve eşik rengi de bu yüzdeden hesaplanır.
Alan yoksa 0 kabul edilir.
