// js/main.js

document.getElementById('check').addEventListener('click', () => {
    const password = document.getElementById('password').value;
    const feedback = document.getElementById('feedback');
    
    const result = getPasswordFeedback(password);
    feedback.innerHTML = result.message;
});

function getPasswordFeedback(password) {
    const minLength = 8;
    const criteria = [
        { regex: /.{8,}/, message: 'At least 8 characters' },
        { regex: /[A-Z]/, message: 'At least one uppercase letter' },
        { regex: /[a-z]/, message: 'At least one lowercase letter' },
        { regex: /[0-9]/, message: 'At least one number' },
        { regex: /[!@#$%^&*(),.?":{}|<>]/, message: 'At least one special character' }
    ];

    let valid = true;
    let messages = [];

    criteria.forEach(criterion => {
        if (!criterion.regex.test(password)) {
            valid = false;
            messages.push(criterion.message);
        }
    });

    return {
        valid: valid,
        message: valid ? 'Password is strong!' : 'Password is weak. ' + messages.join(', ')
    };
}
