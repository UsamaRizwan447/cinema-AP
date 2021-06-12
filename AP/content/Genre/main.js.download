//$('#ian').text('0418131546');
jQuery(function($) {'use strict',

    //#main-slider
    $(function(){
        $('#main-slider.carousel').carousel({
            interval: 8000
        });
    });

    // collapses footer seo links and expands with one link
    $('#quick-link-location-container').hide();
    $('#quick-link-location i').addClass('fa-plus-square-o');
    $('#quick-link-location').on('click', function(e) {
        $this = $(this);
        $('#quick-link-location-container').toggle(function(e) {
            if ( $('#quick-link-location-container').is( ':visible' ) ) {
                $('i', $this).addClass('fa-minus-square-o');
                $('i', $this).removeClass('fa-plus-square-o');
            } else {
                $('i', $this).addClass('fa-plus-square-o');
                $('i', $this).removeClass('fa-minus-square-o');
            }

        });
        /*
         $('#quick-link-location-container').show(function() {
         $("#quick-link-location-container").animate({ scrollTop: $('#quick-link-location-container').prop("scrollHeight")}, 100);
         });*/

        e.preventDefault();
    });

    // fallback for collapsing SEO quicklinks
    $('[data-toggle="collapse"]').on('click', function(e) {
        // use this if bootstrap.js is not loaded
        if(typeof($.fn.collapse) === 'undefined') {
            var target = $(this).attr('data-target');

            $('.collapse.in').slideUp(250, function() {
                $(this).removeClass('in');
            });

            if(!$(target).hasClass('in')) {
                $(target).slideDown(250, function() {
                    $(this).addClass('in');
                });
            }
        }

        e.preventDefault();
    });

    // accordian
    $('.accordion-toggle').on('click', function(){
        $(this).closest('.panel-group').children().each(function(){
            $(this).find('>.panel-heading').removeClass('active');
        });

        $(this).closest('.panel-heading').toggleClass('active');
    });

    //Initiat WOW JS
    new WOW().init();

    // portfolio filter
    $(window).load(function(){'use strict';
        var $portfolio_selectors = $('.portfolio-filter >li>a');
        var $portfolio = $('.portfolio-items');
        $portfolio.isotope({
            itemSelector : '.portfolio-item',
            layoutMode : 'fitRows'
        });

        $portfolio_selectors.on('click', function(){
            $portfolio_selectors.removeClass('active');
            $(this).addClass('active');
            var selector = $(this).attr('data-filter');
            $portfolio.isotope({ filter: selector });
            return false;
        });
    });

    // Contact form
    var form = $('#main-contact-form');
    form.submit(function(event){
        event.preventDefault();
        var form_status = $('<div class="form_status"></div>');
        $.ajax({
            url: $(this).attr('action'),

            beforeSend: function(){
                form.prepend( form_status.html('<p><i class="fa fa-spinner fa-spin"></i> Email is sending...</p>').fadeIn() );
            }
        }).done(function(data){
            form_status.html('<p class="text-success">' + data.message + '</p>').delay(3000).fadeOut();
        });
    });


    //goto top
    $('.gototop').click(function(event) {
        event.preventDefault();
        $('html, body').animate({
            scrollTop: $("body").offset().top
        }, 500);
    });

    //Pretty Photo
    $("a[rel^='prettyPhoto']").prettyPhoto({
        social_tools: false
    });
});




