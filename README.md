# Word Belgesi Çeviri Servisi

Bir klasördeki tüm `.docx` dosyalarını tek istekle birden çok dile çeviren, belge yapısını koruyan REST servisi. Kullanım kılavuzları ve teknik dokümanların çok dilli sürümlerini hazırlamak için yazıldı.

> Bu depo bir proje vitrinidir. Kaynak kod paylaşılmamaktadır.

## Özellikler

- Başlıkları, paragrafları ve tablo hücrelerini çevirir; temel biçimlendirme korunur
- Tek istekte birden çok hedef dil
- Büyük klasörler arka plan görevi olarak işlenir; görev durumu `task_id` ile sorgulanır
- LLM tabanlı çeviri (DeepSeek API), dil başına ayrı çıktı klasörü

## API

```
POST /translate          { "directory_path": "...", "target_languages": ["Turkish", "German"] }
GET  /tasks/{task_id}    → ilerleme ve sonuç
```

## Teknolojiler

`Python` · `FastAPI` · `python-docx` · `DeepSeek API` · `BackgroundTasks`
