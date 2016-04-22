---
layout: page-fullwidth
title: "İletişim"
teaser: "Bize ulaşın!"
permalink: "/iletisim/"
header: no
address: Izmir Yuksek Teknoloji Enstitusu
mail: info@zetaops.io

---

<div class="container">
    <div class="row">
        <div class="large-6 columns">
            <h3>Harita</h3>
            <div class="google-map h-250 space-bottom"
                 data-location="{{ page.address }}" data-zoom="12">
                <div id="map-canvas"></div>
            </div>
        </div>
        <div class="large-6 columns" id="contact">
            <h3>İletişim Formu</h3>
            <form action="https://formspree.io/{{ page.mail }}" method="POST">
                <input type="text" name="_gotcha" style="display:none" />
                <input type="text" name="name" placeholder="Isim Soyisim, Nick">
                <input type="email" name="_replyto" placeholder="Mail">
                <textarea type="text" name="message" placeholder="Mesaj"></textarea>
                <input class="button radius" style="float:right;" type="submit" value="Mesaj Gönderin">
            </form>
        </div>
    </div>
    <div class="row">
        <div class="large-6 columns">
            <h5>Adres:</h5>
            <p>Gülbahçe Mah. İzmir Teknoloji Geliştirme Bölgesi A9 Blok 215/A IYTE Campus,
                URLA/IZMIR</p>
            <h5>Telefon:</h5>
            <p>+90 232 502 08 57</p>
            <h5>E-posta:</h5>
            <p><span id="epo" class="linky">info(asyouknow)zetaops.io</span></p>
        </div>
        <div class="large-6 columns">
            <img src="{{site.urlimg}}zops-enginar-400-small.jpg" style="width: 50%; height: 50%">
        </div>
    </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.3/jquery.min.js"></script>
<script type="text/javascript"
        src="https://maps.googleapis.com/maps/api/js?key=AIzaSyA5DLwPPVAz88_k0yO2nmFe7T9k1urQs84"></script>
<script src="/assets/js/maps.js"></script>