
        let index = 0;
        const images = document.querySelectorAll('.carousel img');
        
        function showNextImage() {
            images[index].style.transform = 'translateX(-100%)';
            index = (index + 1) % images.length;
            images[ setInterval(showNextImage, 3000
