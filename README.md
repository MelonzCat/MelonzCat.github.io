# MelonzCat.github.io
const names = [
  'Aru',
  'Shiroko',
  'Yakuu',
  'Kasane Teto',
  'Emilia',
  'Reze',
  'Alya',
  'Rias Gremory',
  'Asuka',
  'Yor'
];

document.body.innerHTML = `
  <main class="page">
    <p class="subtitle">My Top 10 Simps</p>
    <h1>MelonzSimp</h1>
    <ol>${names.map(name => `<li>${name}</li>`).join('')}</ol>
    <p class="created-by">Created By MelonzCat</p>
  </main>
`;

document.title = 'MelonzSimp';

document.head.insertAdjacentHTML('beforeend', `
  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 48px 16px;
      background: #22c55e;
      font-family: Arial, sans-serif;
    }

    .page {
      width: 100%;
      max-width: 512px;
      text-align: center;
    }

    .subtitle, .created-by {
      color: rgba(255, 255, 255, 0.9);
      font-weight: 600;
      letter-spacing: 0.04em;
    }

    .subtitle { margin: 0 0 4px; font-size: 1.125rem; }

    h1 {
      margin: 0 0 32px;
      color: white;
      font-size: 2.25rem;
      letter-spacing: 0.04em;
    }

    ol {
      width: 100%;
      margin: 0;
      padding: 24px 32px;
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.92);
      box-shadow: 0 10px 15px rgba(0, 0, 0, 0.15);
      list-style: none;
      counter-reset: simp;
      text-align: left;
    }

    li {
      display: flex;
      align-items: center;
      gap: 12px;
      margin: 12px 0;
      color: #1f2937;
      font-size: 1.125rem;
      counter-increment: simp;
    }

    li::before {
      width: 24px;
      color: #16a34a;
      font-weight: 700;
      text-align: right;
      content: counter(simp) '.';
    }

    .created-by { margin: 24px 0 0; }
  </style>
`);
