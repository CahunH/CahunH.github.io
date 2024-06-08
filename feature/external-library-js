// js/main.js

document.getElementById('check').addEventListener('click', () => {
    const password = document.getElementById('password').value;
    const feedback = document.getElementById('feedback');
    
    const result = zxcvbn(password);
    feedback.innerHTML = getFeedbackMessage(result);
});

function getFeedbackMessage(result) {
    const messages = [
        "Very weak",
        "Weak",
        "Medium",
        "Strong",
        "Very strong"
    ];
    
    return `Password strength: ${messages[result.score]}<br>${result.feedback.suggestions.join('<br>')}`;
}
