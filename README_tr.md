# Derin Araştırma Web Arayüzü

[[English](README.md) | [中文](README_zh.md) | Türkçe]

Bu, https://github.com/dzhng/deep-research için çeşitli iyileştirmeler ve düzeltmeler içeren bir web arayüzüdür.

Özellikler:

- 🚀 **Güvenli**: Her şey (yapılandırma, API istekleri, ...) yerel olarak tarayıcınızda kalır
- 🕙 **Gerçek zamanlı geri bildirim**: Yapay zeka yanıtlarını akış olarak alın ve arayüzde gerçek zamanlı olarak görüntüleyin
- 🌳 **Arama görselleştirme**: Araştırma sürecini ağaç yapısı kullanarak gösterir. Farklı dillerde arama yapmayı destekler
- 📄 **PDF olarak dışa aktarma**: Nihai araştırma raporunu Markdown / PDF olarak dışa aktarın
- 🤖 **Daha fazla model desteği**: Yapılandırılmış Çıktılar gibi daha yeni, daha az yaygın olarak desteklenen özellikler yerine düz komutlar kullanır. Bu, en son OpenAI yeteneklerine ayak uyduramayan daha fazla sağlayıcıyla çalışmasını sağlar.
- 🐳 **Docker desteği**: Tek satırlık komutla kendi ortamınızda dağıtın

Şu anda mevcut sağlayıcılar:

- Yapay Zeka: OpenAI uyumlu, SiliconFlow, Infiniai, DeepSeek, OpenRouter, Ollama ve daha fazlası
- Web Arama: Tavily (ayda 1000 ücretsiz kredi), Firecrawl (bulut / kendi barındırdığınız)

Bu projeyi beğendiyseniz lütfen bir 🌟 Yıldız verin!

<video width="500" src="https://github.com/user-attachments/assets/8f9baa43-a74e-4613-aebb-1bcc29a686f0" controls></video>

## Son güncellemeler

25/03/09

- Eklendi: InifiniAI desteği
- İyileştirilmiş LLM komutları

## Kurulum

### Docker (Önerilen)

```bash
docker run -p 3000:3000 ghcr.io/dzhng/deep-research-web-ui:latest
```

Tarayıcınızda http://localhost:3000 adresini açın.

### Geliştirme

```bash
# Bağımlılıkları yükleyin
npm install

# Geliştirme sunucusunu başlatın
npm run dev
```

## Yapılandırma

İlk kez kullanırken, yapılandırma ayarlarını girmeniz gerekecektir:

1. Bir AI sağlayıcısı seçin ve API anahtarınızı girin
2. Bir Web Arama sağlayıcısı seçin ve API anahtarınızı girin

Tüm yapılandırma yerel olarak tarayıcınızda saklanır ve hiçbir şey sunucuya gönderilmez.

## Nasıl Kullanılır

1. Araştırma konunuzu girin
2. Yapay zeka size bazı takip soruları soracaktır
3. Yapay zeka web'de arama yapacak ve sonuçları bir ağaç yapısında gösterecektir
4. Araştırma tamamlandığında, yapay zeka bir araştırma raporu oluşturacaktır
5. Raporu PDF veya Markdown olarak dışa aktarabilirsiniz

## Katkıda Bulunma

Katkılarınızı memnuniyetle karşılıyoruz! Lütfen bir PR göndermeden önce bir sorun açın.

## Lisans

MIT 