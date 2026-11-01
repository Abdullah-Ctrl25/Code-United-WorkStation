console.log("Script connected successfully!");

const section = document.querySelector('.filter-section');

section.addEventListener('mousemove', (e) => {
  if (Math.random() > 0.3) return;

  const rect = section.getBoundingClientRect();
  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;

  createSparkle(x, y, section);
});

function createSparkle(x, y, parent) {
  const sparkle = document.createElement('div');
  sparkle.classList.add('sparkle');

  // Random size between 6px and 14px
  const size = Math.random() * 16 + 6;
  sparkle.style.width = `${size}px`;
  sparkle.style.height = `${size}px`;

  // Position at cursor
  sparkle.style.left = `${x}px`;
  sparkle.style.top = `${y}px`;

  // Random drift direction using CSS variables
  const tx = (Math.random() - 0.5) * 50;
  const ty = (Math.random() - 0.5) * 50;
  sparkle.style.setProperty('--tx', `${tx}px`);
  sparkle.style.setProperty('--ty', `${ty}px`);

  parent.appendChild(sparkle);

  // Remove element after animation finishes
  setTimeout(() => {
    sparkle.remove();
  }, 800);
}
