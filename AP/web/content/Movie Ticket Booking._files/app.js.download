$(document).ready(function(){

    $( "#clickingDiv" ).click(function() {

        $("#expandDiv").slideToggle("slow");
    });




    //////////////////////////////////////


    $('#docTable').DataTable(
        {
            responsive: true
        });


});






new WOW().init();



$("#clicknumtext").click(function(){

    $("#clicknumtext").fadeOut(300, function() {
        $(this).remove();
        $("#clicknum").fadeIn(300, function() { });
    });
});
$("#clicknumtextother").click(function(){

    $("#clicknumtextother").fadeOut(300, function() {
        $(this).remove();
        $("#clicknumother").fadeIn(300, function() { });
    });

});


function animationHover(element, animation){
    element = $(element);
    element.hover(
        function() {
            element.addClass('animated ' + animation);
        },
        function(){
            //wait for animation to finish before removing classes
            window.setTimeout( function(){
                element.removeClass('animated ' + animation);
            }, 1000);
        }
    );
};
function animationClick(element, animation){
    element = $(element);
    element.click(
        function() {
            element.addClass('animated ' + animation);
            //wait for animation to finish before removing classes
            window.setTimeout( function(){
                element.removeClass('animated ' + animation);
            }, 1000);
        }
    );
};


animationHover('#mainiconimage1', 'flipInX');
animationHover('#mainiconimage2', 'flipInX');
animationHover('#mainiconimage3', 'flipInX');
animationHover('#mainiconimage4', 'flipInX');



animationHover('#quoteButton1', 'flipInX');
animationHover('#quoteButton2', 'flipInX');
animationHover('#quoteButton3', 'flipInX');
animationHover('#quoteButton4', 'flipInX');
animationHover('#quoteButton5', 'flipInX');
animationHover('#quoteButton6', 'flipInX');
