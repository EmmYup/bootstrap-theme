<template>
<div class="home">
  <nav class="navbar navbar-default navbar-fixed-top">
    <div class="container">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
        <a class="navbar-brand" href="#">TechScroll</a>
      </div>
      <div id="navbar" class="collapse navbar-collapse">
        <ul class="nav navbar-nav navbar-right">
          <li><a href="#showcase">Home</a></li>
          <li><a href="#info">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <!--/.nav-collapse -->
    </div>
  </nav>
  <section id="showcase">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-sm-6">
          <div class="showcase-left">
            <img src="../assets/image1.jpg" alt="">
          </div>
        </div>
        <div class="col-md-6 col-sm-6">
          <div class="showcase-right" data-scroll-reveal="enter left and move 50px over 1.33s">
            <h1>Hands-free help from the Google Assistant</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolore eaque accusamus magni a, ab eius illum, esse aliquid animi impedit dolor rem doloremque quo quae asperiores ea consequuntur qui deleniti.</p>
          </div>
          <br>
          <a href="" class="btn btn-default btn-lg showcase-btn">Read more</a>
        </div>
      </div>
    </div>
  </section>
  <section id="testimonial">
    <div class="container">
      <p>"Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nostrum earum magni eos blanditiis beatae. Fugit sed quidem ipsa assumenda ut voluptatem saepe, dolores."</p>
      <p class="customer">- John Doe</p>
    </div>
  </section>
  <section id="info">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-sm-6">
          <div class="info-left">
            <img src="../assets/image2.png" alt="">
          </div>
        </div>
        <div class="col-md-6 col-sm-6">
          <div class="info-right">
            <h2>Get to Know Google Home</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus ipsum, aliquam! Voluptatibus ea sequi quis laborum, ab consequuntur numquam omnis corrupti suscipit, cupiditate nisi. Natus corporis id necessitatibus error officiis.</p>
          </div>
          <br>
          <a href="" class="btn btn-default btn-lg">Read more</a>
        </div>
      </div>
    </div>
  </section>
  <hr>
  <section id="info2">
    <div class="container">
      <div class="row">
        <div class="col-md-6 col-sm-6">
          <div class="info-left">
            <h2>Info Blog One</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus ipsum, aliquam! Voluptatibus ea sequi quis laborum, ab consequuntur numquam omnis corrupti suscipit, cupiditate nisi. Natus corporis id necessitatibus error officiis.</p>
          </div>
        </div>
        <div class="col-md-6 col-sm-6">
          <div class="info-right">
            <h2>Info Blog Two</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus ipsum, aliquam! Voluptatibus ea sequi quis laborum, ab consequuntur numquam omnis corrupti suscipit, cupiditate nisi. Natus corporis id necessitatibus error officiis.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section id="contact">
    <div class="container">
      <div class="row">
        <div class="col-md-5 col-sm-5">
          <form>
            <div class="form-group">
              <label>Name: </label>
              <input class="form-control" type="text" name="" value="" placeholder="Enter Name">
            </div>
            <div class="form-group">
              <label>Email: </label>
              <input class="form-control" type="text" name="" value="" placeholder="Enter Email">
            </div>
            <div class="form-group">
              <label>Message: </label>
              <textarea class="form-control" name="" value="" placeholder="Enter Message"></textarea>
            </div>
            <button class="btn btn-default">Submit</button>
          </form>
        </div>
        <div class="col-md-7 col-sm-7">

        </div>
      </div>
    </div>
  </section>
  <footer>
    <p class="text-center">TechScroll Copyright &copy; 2017</p>
  </footer>
</div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {}
  },
  created() {
    window.sr = ScrollReveal()
  },
  mounted() {
    sr.reveal('.navbar', {
      duration: 2000,
      origin: 'bottom'
    });
    sr.reveal('.showcase-left', {
      duration: 2000,
      origin: 'top',
      distance: '300px'
    });
    sr.reveal('.showcase-right', {
      duration: 2000,
      origin: 'right',
      distance: '300px'
    });
    sr.reveal('.showcase-btn', {
      duration: 2000,
      delay: 2000,
      origin: 'bottom'
    });
    sr.reveal('#testimonial div', {
      duration: 2000,
      origin: 'bottom'
    });
    sr.reveal('.info-left', {
      duration: 2000,
      origin: 'left',
      distance: '300px',
      viewFactor: 0.2
    });
    sr.reveal('.info-right', {
      duration: 2000,
      origin: 'right',
      distance: '300px',
      viewFactor: 0.2
    });
    $(function() {
      // Smooth Scrolling
      $('a[href*="#"]:not([href="#"])').click(function() {
        if (location.pathname.replace(/^\//, '') == this.pathname.replace(/^\//, '') && location.hostname == this.hostname) {
          var target = $(this.hash);
          target = target.length ? target : $('[name=' + this.hash.slice(1) + ']');
          if (target.length) {
            $('html, body').animate({
              scrollTop: target.offset().top
            }, 1000);
            return false;
          }
        }
      });
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
