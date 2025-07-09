document.addEventListener('DOMContentLoaded', function() {
    const gallery = document.querySelector('.gallery-container');
    const images = document.querySelectorAll('.image-wrapper');
    const heartButton = document.querySelector('.heart-button');
    let currentIndex = 0;
    
    // Function to transition to next image
    function transitionToNextImage() {
        // Fade out current image
        images[currentIndex].classList.remove('active');
        
        // Calculate next index
        currentIndex = (currentIndex + 1) % images.length;
        
        // Fade in next image
        images[currentIndex].classList.add('active');
        
        // Add romantic effect
        createHearts();
    }
    
    // Create floating hearts effect
    function createHearts() {
        for (let i = 0; i < 10; i++) {
            const heart = document.createElement('div');
            heart.innerHTML = '❤️';
            heart.style.position = 'absolute';
            heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.top = Math.random() * 100 + '%';
            heart.style.opacity = '0';
            heart.style.transform = 'translateY(0) scale(0)';
            heart.style.transition = 'all 2s ease-out';
            heart.style.zIndex = '5';
            heart.style.pointerEvents = 'none';
            
            gallery.appendChild(heart);
            
            // Trigger animation
            setTimeout(() => {
                heart.style.opacity = '0.7';
                heart.style.transform = `translateY(-${Math.random() * 100 + 50}px) scale(1)`;
            }, 10);
            
            // Remove heart after animation
            setTimeout(() => {
                heart.remove();
            }, 2000);
        }
    }
    
    // Click event for heart button
    heartButton.addEventListener('click', transitionToNextImage);
    
    // Touch event for mobile devices
    heartButton.addEventListener('touchend', function(e) {
        e.preventDefault();
        transitionToNextImage();
    });
    
    // Optional: Auto-advance every 5 seconds
    // setInterval(transitionToNextImage, 5000);
    
    // Initialize first image
    images[0].classList.add('active');
});

