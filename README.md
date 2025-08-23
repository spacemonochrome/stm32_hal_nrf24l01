<<<<<<< HEAD
# STM32 HAL NRF24L01 Kütüphanesi ve Örnekleri

Bu proje, STM32 mikrodenetleyicilerinde HAL kütüphanesi ile NRF24L01 kablosuz modülünü kullanarak veri iletimi ve alımı için geliştirilmiş C sürücüsü ve örnek uygulamaları içerir.

## Klasör Yapısı

- `rx-tx/nrf24l01/` : NRF24L01 sürücü dosyaları (C ve header)
- `rx-tx/nrf24L01_F103C8T6/` : STM32F103C8T6 için gönderici (TX) örnek uygulama
- `rx-tx/nrf24L01_F407VGT6/` : STM32F407VGT6 için alıcı (RX) örnek uygulama

## Sürücü Özellikleri

- SPI üzerinden NRF24L01 ile haberleşme
- Veri hızı, güç, kanal, adres, CRC, otomatik tekrar gibi tüm temel ayarların yapılabilmesi
- Dinamik ve sabit payload desteği
- Otomatik ve manuel ACK yönetimi
- FIFO yönetimi, hata ve durum okuma fonksiyonları

### Temel Fonksiyonlar

- `nrf24_init()` : Modül başlatma
- `nrf24_transmit()` : Veri gönderme
- `nrf24_receive()` : Veri alma
- `nrf24_set_channel()`, `nrf24_tx_pwr()`, `nrf24_data_rate()` : Temel ayarlar
- Tüm fonksiyonlar için detaylı açıklamalar `nrf24l01/NRF24.h` dosyasında mevcuttur.

## Örnek Uygulamalar

### Gönderici (STM32F103C8T6)

`rx-tx/nrf24L01_F103C8T6/Core/Src/main.c` dosyasında temel olarak:

- SPI ve GPIO başlatılır
- NRF24 başlatılır ve TX moduna alınır
- Belirli aralıklarla veri gönderilir

### Alıcı (STM32F407VGT6)

`rx-tx/nrf24L01_F407VGT6/Core/Src/main.c` dosyasında temel olarak:

- SPI ve GPIO başlatılır
- NRF24 başlatılır ve RX moduna alınır
- Gelen veri okunur ve işlenir

## Donanım Bağlantısı

- SPI pinleri ve CE/CSN pinleri `NRF24_conf.h` dosyasında tanımlanır
- Her iki kartta da SPI1 ve GPIOA kullanılmıştır (örnek olarak)

## Derleme ve Kullanım

1. İlgili STM32CubeIDE projesini açın
2. Kendi donanımınıza göre pinleri ve SPI ayarlarını güncelleyin
3. Kodları derleyip kartınıza yükleyin

## Lisans

Sürücü ve örnekler MIT lisansı ile sunulmaktadır. STM32 HAL ve CMSIS dosyaları STMicroelectronics'e aittir.
=======
# stm32_hal_nrf24l01

referance; https://github.com/developer328/stm32_hal_nrf24_library

How To Use
https://teslaninsovalyesi.blogspot.com/2025/08/stm32-nrf24l01-11-rx-tx-ornegi.html
>>>>>>> f25d258f005b2accf2d474d3faa4918954984a24
