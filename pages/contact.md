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
            <span class="subject" style="font-weight:bold;color:red;"></span>
            <form action="https://formspree.io/{{ page.mail }}" method="POST">
                <input type="text" name="name" placeholder="Isim Soyisim, Nick">
                <input type="email" name="_replyto" placeholder="Mail">
                <textarea type="text" name="message" placeholder="Mesaj"></textarea>
                <input class="button radius" style="float:right;" type="submit" value="Mesaj Gönderin">
                <!-- Hidden form Elements -->
                <input type="text" class="subject" name="_subject" style="display:none" value="Diğer" />
                <input type="text" name="_gotcha" style="display:none" />
                <input type="hidden" name="_next" value="{{site.url}}/thanks" />
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


<script src="{{ site.url }}/assets/js/jquery-2.2.3.min.js"></script>
<script type="text/javascript"
        src="https://maps.googleapis.com/maps/api/js?key=AIzaSyA5DLwPPVAz88_k0yO2nmFe7T9k1urQs84"></script>
<script src="/assets/js/contact.js"></script>

<script>
var QueryString = function () {
    var query_string = {};
    var query = window.location.search.substring(1);
    var vars = query.split("&");
    for (var i=0;i<vars.length;i++) {
        var pair = vars[i].split("=");
        // If first entry with this name
        if (typeof query_string[pair[0]] === "undefined") {
            query_string[pair[0]] = decodeURIComponent(pair[1]);
            // If second entry with this name
        } else if (typeof query_string[pair[0]] === "string") {
            var arr = [ query_string[pair[0]],decodeURIComponent(pair[1]) ];
            query_string[pair[0]] = arr;
            // If third or later entry with this name
        } else {
            query_string[pair[0]].push(decodeURIComponent(pair[1]));
        }
    }
    return query_string;
}();


if (parseInt(QueryString.place) && parseInt(QueryString.job)){
    var placeObj = {{ site.places | jsonify }};
    try{
        var place = placeObj[QueryString.place-1].name;
        var job = placeObj[QueryString.place-1].jobs[QueryString.job-1].name;
        $('.subject').val(place+" - "+job+" [personel-ik]");
        $('.subject').html(place+" - "+job);

    }
    catch(err){
        console.log("Yanlis parametre girildi.")
    }
}
</script>