# ReinforcementLearning_DQNPathPlanner
Pekiştirmeli Öğrenme (Reinforcement Learning), insanların hedeflerine ulaşmak için kullandığı deneme yanılma yöntemini taklit eden bir makine öğrenimi tekniğidir. Bu yöntem, ajanların belirli bir ortamda verilen ödülleri maksimize etmek için hangi eylemleri gerçekleştirmeleri gerektiğini öğrenmelerini sağlamaktadır. Ajanlar, her eylem için aldıkları geri bildirimleri kullanarak ödül ve ceza paradigması çerçevesinde verileri işlemektedir. Bu süreç, tekrarlanan denemeler ve hatalar yoluyla gerçekleşmektedir. Ajan, aldığı geri bildirimlerden yararlanarak en iyi davranış stratejilerini keşfedip uygulamaktadır.

RL doğası gereği uzun vadeli ödül maksimizasyonu sağlamak için gereken eylemleri belirlemektedir. Buradaki temel amaç ajanın hem başarılı hem de başarısız deneyimlerinden öğrenerek daha etkili kararlar almasını sağlamaktır. Bu özellikleriyle RL, karmaşık ve dinamik ortamlarda etkili kararlar almak için güçlü bir yöntem olarak öne çıkmaktadır.Pekiştirmeli öğrenme; ajan (agent) adı verilen öğrenen bir sistem, durum (state), eylem (action) ve ödül (reward) unsurlarının etkileşimi üzerine kuruludur.

### Pekiştirmeli Öğrenme (Reinforcement Learning) algoritmasının temel kavramları aşağıda açıklanmıştır:
- Ajan (Agent): Bir ödül kazanmak için bir ortamda eylemler gerçekleştiren varsayımsal 
varlıktır.
- Eylem (Action, a): Ajanın yapabileceği tüm olası hamleleri ifade etmektedir. 
- Ortam (Environment): Ajanın içinde bulunduğu ve etkileşimde bulunduğu senaryoyu ifade etmektedir. 
- Durum (State, s): Ortamın döndürdüğü mevcut durumu ifade etmektedir. 
- Ödül (Reward, r): Ajanın son eylemini değerlendirmek için ortamdan gönderilen anında geri dönüştür. 
- Politika (Policy, π): Ajanın mevcut duruma göre bir sonraki eylemi belirlemek için kullandığı stratejidir.
- Durum Değeri (Value Function): Kısa vadeli ödül R'nin aksine, iskontolu beklenen uzun vadeli getiri. Vπ(s) , π politikası kapsamında mevcut durum s'nin beklenen uzun vadeli getirisi olarak tanımlanır.
- Q Değeri veya Eylem Değeri: Q değeri, geçerli eylem a olan ekstra bir parametre alması dışında Değer'e benzer, Qπ(s, a), π politikası kapsamında a eylemi gerçekleştirerek mevcut s durumunun uzun vadeli geri dönüşünü ifade etmektedir.

Aşağıdaki görsellerde, eğitim süreci Kaggle platformunda gerçekleştirilmiştir. Bu süreçte, modelin en iyi çıktıları verebilmesi için uygun hiperparametreler denenmiş ve loss grafikleri analiz edilmiştir.
![1](https://github.com/user-attachments/assets/066c00bb-3ff7-4528-8a60-b9b2311bc3d0)   
![2](https://github.com/user-attachments/assets/8978400d-949c-47ad-aed4-c6a3bd811421)

Hiperparametreler, öğrenme oranı (learning rate), epsilon (ε), epsilon decay ve gamma (γ) gibi önemli değerlerden oluşmaktadır. Öğrenme oranı modelin öğrenme hızını, epsilon ve epsilon decay ise ajanın keşif ve sömürü dengesini kontrol etmektedir. Gamma değeri ise gelecekteki ödüllerin anlık kararlar üzerindeki etkisini belirlemektedir.

İlgili parametreler, aşağıdaki görselde yer alan kodda gösterilmektedir.
![3](https://github.com/user-attachments/assets/bc7fce54-f5dc-4a3b-9302-0e74355e2d6d)

Bu repoda grid tabanlı bir harita üzerinde çalışılmıştır. Grid tabanlı harita üzerinde birer adet başlangıç ve bitiş noktası belirlenmiştir. İlk hedef olarak ajanın başlangıç noktasından bitiş noktasına kendi kendine gitmesi hedeflenmiştir. Ajanın ne kadar iyi öğrendiğini tespit edebilmek için bir test kodu yazılmış ve her test sonucunda başlangıç ve bitiş noktaları random olarak belirlenmiştir. Sonuçların daha iyi yorumlanabilmesi için ajanın yolu görselleştirilmiştir.
![1](https://github.com/user-attachments/assets/9a0f33d0-853f-4881-a321-69a38b5004d8)
![2](https://github.com/user-attachments/assets/06fbce5d-4992-4394-9364-91178b654b50)




