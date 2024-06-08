// js/main.js

document.getElementById('check').addEventListener('click', () => {
    const password = document.getElementById('password').value;
    const feedback = document.getElementById('feedback');
    
    const isValid = validatePassword(password);
    feedback.textContent = isValid ? 'Password is valid' : 'Password is invalid';
});

function validatePassword(password) {
    const minLength = 8;
    const hasUpperCase = /[A-Z]/.test(password);
    const hasLowerCase = /[a-z]/.test(password);
    const hasNumbers = /[0-9]/.test(password);
    const hasSpecialChars = /[!@#$%^&*(),.?":{}|<>]/.test(password);

    return password.length >= minLength && hasUpperCase && hasLowerCase && hasNumbers && hasSpecialChars;
}
