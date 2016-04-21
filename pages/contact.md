---
layout: page-fullwidth
title: "İletİşİm"
teaser: Formumuzu kullanarak bize ulasabilirsiniz
permalink: "/iletisim/"
header: no
location:
    address: Izmir Yuksek Teknoloji Enstitusu
    latitude: 38.3148372
    longitude: 26.6361488
---

<div class="container">
    <div class="row">
        <!--Featured Posts-->
        <div class="col-md-8 col-sm-8">
            <h3>Harİta</h3>
            <!--Google Map-->
            <div class="google-map h-250 space-bottom"
                 data-location="Izmir Yuksek Teknoloji Enstitusu" data-zoom="12">
                <!--Insert Location in data-location, insert map zoom in data-zoom-->
                <div id="map-canvas"></div>
            </div>
            <!--Google Map Close-->
        </div>
        <!--Contact Info-->
        <div class="col-md-4 col-sm-4" id="contact">
            <div class="contacts">
                <h5>Adres:</h5>
                <p>Gülbahçe Mah. İzmir Teknoloji Geliştirme Bölgesi A9 Blok 215/A IYTE Campus,
                    URLA/IZMIR</p>
                <h5>Telefon:</h5>
                <p>+90 232 502 08 57</p>
                <h5>E-posta:</h5>
                <p><span id="epo" class="linky">info(asyouknow)zetaops.io</span></p>
                <div class="social-bar">
                    <img src="{{site.urlimg}}zops-enginar-400-small.jpg" style="width: 50%; height: 50%">
                </div>
            </div>
        </div>
    </div>
</div>
<form action="https://formspree.io/info@zetaops.io"
      method="POST">
    <input type="text" name="name" placeholder="Isim, Soyisim">
    <input type="email" name="_replyto" placeholder="Mail">
    <textarea type="text" name="message" placeholder="Message">
    </textarea>
    <input type="submit" value="Send">
</form>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.3/jquery.min.js"></script>
<script type="text/javascript"
        src="https://maps.googleapis.com/maps/api/js?key=AIzaSyA5DLwPPVAz88_k0yO2nmFe7T9k1urQs84"></script>
<script src="/assets/js/maps.js"></script>