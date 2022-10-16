---
selector: kontakt
header: kontakt
title: Auf diesen <span>Wegen</span> findest du uns
layout: default
order: 5
---


<div class="row justify-content-md-center text-center">
    <div class="col-lg-10 col-md-10 d-flex align-items-stretch">
        <iframe style="border:0; width: 100%; height: 550px;" 
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2711.400260367478!2d7.7052483!3d47.18917779999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x478e2b6d5927f0af%3A0x98c84f9de5ea1b9c!2sKinderb%C3%B6rse%20Kleiner%20Fuchs!5e0!3m2!1sen!2sch!4v1660504657171!5m2!1sen!2sch" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
</div>

<div class="row justify-content-md-center" style="padding-top: 2em">
    <div class="col-lg-10 col-md-10">
        <div class="row gy-4 g-3 row-cols-lg-2 row-cols-md-1 row-cols-sm-1">
            <div class="col">
              <div class="info-item  d-flex align-items-center">
                <i class="icon bi bi-map flex-shrink-0"></i>
                <div>
                  <h3>Adresse</h3>
                  <p>Wangenstrasse 20, 3360&nbsp;Herzogenbuchsee</p>
                </div>
              </div>
            </div>
            <div class="col">
              <div class="info-item d-flex align-items-center">
                <i class="icon bi bi-envelope flex-shrink-0"></i>
                <div>
                  <h3>Email</h3>
                  <p>kinderboerse.kleinerfuchs@gmail.com</p>
                </div>
              </div>
            </div>
            <div class="col">
              <div class="info-item  d-flex align-items-center">
                <i class="icon bi bi-telephone flex-shrink-0"></i>
                <div>
                  <h3>Telefon Chrigä</h3>
                  <p>{{site.phone_chrige}}</p>
                </div>
              </div>
            </div>
            <div class="col">
              <div class="info-item  d-flex align-items-center">
                <i class="icon bi bi-telephone flex-shrink-0"></i>
                <div>
                  <h3>Telefon Michèle</h3>
                  <p>{{site.phone_michele}}</p>
                </div>
              </div>
            </div>
          </div>
    </div>
</div>

<script src="https://www.google.com/recaptcha/api.js?render=6Ld2XYYiAAAAAFxht8gz5zAdbYpoLQjklEvDt_oy"></script>
<script>
    function onClick(e) {
        e.preventDefault();
        grecaptcha.ready(function() {
            grecaptcha.execute('6Ld2XYYiAAAAAFxht8gz5zAdbYpoLQjklEvDt_oy', {action: 'submit'}).then(function(token) {
                document.getElementById('g-recaptcha-response').value = token;
                console.log('>>> ', token);
                });
                });
    }
</script>
<div id="kontakt-form" class="row justify-content-md-center text-center" style="padding-top: 2em">
    <div class="col-lg-10 col-md-10">
        <form action="https://formkeep.com/f/ea741f9c0375"
           accept-charset="UTF-8" enctype="multipart/form-data" method="POST" class="email-form p-3 p-md-4">
            <input type="hidden" id="g-recaptcha-response" name="g-recaptcha-response">
            <div class="row">
              <div class="col-xl-6 form-group">
                <input type="text" name="name" class="form-control" id="name" placeholder="Dein Name" required>
              </div>
              <div class="col-xl-6 form-group">
                <input type="email" class="form-control" name="email" id="email" placeholder="Deine Email" required>
              </div>
            </div>
            <div class="form-group">
              <input type="text" class="form-control" name="subject" id="subject" placeholder="Titel" required>
            </div>
            <div class="form-group">
              <textarea class="form-control" name="message" rows="5" placeholder="Message" required></textarea>
            </div>
            <div class="my-3">
              <div class="loading">Loading</div>
              <div class="error-message"></div>
              <div class="sent-message">Deine Nachricht wurde übermittelt. Merci!</div>
            </div>
            <div class="text-center" style="padding-top: 1em">
                <button type="submit" onclick="onClick">Abschicken</button>
                <input type="hidden" name="utf8" value="✓">
            </div>
          </form>
  </div>
</div>
