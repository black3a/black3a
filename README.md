- 👋 Hi, I’m @black3a
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
black3a/black3a is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import numpy as np

# Basit bir alım satım stratejisi
def trading_strategy(data):
    buy_signal = False
    sell_signal = False
    
    # Örnek alım satım stratejisi (örneğin 50 günlük ve 200 günlük hareketli ortalama stratejisi)
    if data['50 günlük hareketli ortalama'] > data['200 günlük hareketli ortalama']:
        buy_signal = True
    elif data['50 günlük hareketli ortalama'] < data['200 günlük hareketli ortalama']:
        sell_signal = True
        
    return buy_signal, sell_signal

# Örnek veri
data = {
    '50 günlük hareketli ortalama': np.random.rand(100),
    '200 günlük hareketli ortalama': np.random.rand(100)
}

# Stratejiyi uygulama
buy_signal, sell_signal = trading_strategy(data)

if buy_signal:
    print("Alım sinyali oluşturuldu!")
elif sell_signal:
    print("Satış sinyali oluşturuldu!")
else:
    print("Beklemede kalın.")
