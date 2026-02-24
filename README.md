document.addEventListener('DOMContentLoaded', () => {
    const menuItems = [
        { name: 'Burger', price: 'R29.00 Mini Burger - R39.00 X-tra Mini - 60 Monster Mini-Mee!' },
        { name: 'Fries', price: 'R15.00 Small - R20.00 Medium - R40.00 Large' },
        { name: 'Pizza', price: 'R15.00 Single - R30.00 Medium Single, (Double: + R5.00 incl.)- R60.00 Monster Large' },
        { name: 'Salad', price: 'R4.99' },
    ];

    const menuList = document.getElementById('food-menu');
    
    menuItems.forEach(item => {
        const li = document.createElement('li');
        li.textContent = `${item.name} - ${item.price}`;
        menuList.appendChild(li);
    });

    const contactForm = document.getElementById('contact-form');
    contactForm.addEventListener('submit', (e) => {
        e.preventDefault();
        alert('Thank you for contacting us!');
        contactForm.reset();
    });
});
