1. CSS Animation
Use @keyframes to animate elements:

css
@keyframes bounce {
  0% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0); }
}

button {
  animation: bounce 0.5s infinite;
}


2. JavaScript: Store & Retrieve User Preferences
Use localStorage to save user selections:

js
function savePreference(key, value) {
  localStorage.setItem(key, value);
}

function getPreference(key) {
  return localStorage.getItem(key);
}

// Example usage
savePreference("theme", "dark");
console.log(getPreference("theme")); // Outputs: "dark"

3. Trigger Animation with JavaScriptDynamically trigger an animation on user interaction:

js
document.getElementById("animate-btn").addEventListener("click", function() {
  this.style.transition = "transform 0.5s ease-in-out";
  this.style.transform = "scale(1.2)";
  setTimeout(() => this.style.transform = "scale(1)", 500);
});
