<script>
  const storeUrl = 'https://smartstore.naver.com/benasis'
  const youtubeUrl = 'https://www.youtube.com/@cwj-2025'
  const blogUrl = 'https://blog.naver.com/cojhhhhh'
  const avatarUrl = '/smartstore-로고.jpg'
</script>

<svelte:head>
  <title>최원준가구갤러리</title>
  <meta name="description" content="최원준가구갤러리 스마트스토어 링크" />
</svelte:head>

<main class="page linktree">
  <section class="tree-card">
    <div class="avatar-wrap" aria-hidden="true">
      <img class="avatar-image" src={avatarUrl} alt="스마트스토어 로고" />
    </div>
    <h1 class="brand-title">최원준가구갤러리</h1>
    <p class="brand-handle">@jun3.3</p>
    <nav class="link-list" aria-label="외부 링크">
      <a class="link-btn ssprimary" href={storeUrl} target="_blank" rel="noopener noreferrer">
        네이버 스마트스토어 방문하기
      </a>
      <a class="link-btn blprimary" href={blogUrl} target="_blank" rel="noopener noreferrer">
        네이버 블로그 방문하기
      </a>
      <a class="link-btn ytprimary" href={youtubeUrl} target="_blank" rel="noopener noreferrer">
        공식 유튜브 방문하기
      </a>
    </nav>
  </section>
</main>

<style>
  .linktree {
    min-height: calc(100vh - (var(--page-shell-pad) * 2));
    margin-bottom: 0;
    display: grid;
    place-items: center;
    width: 100%;
    padding: clamp(12px, 4vw, 32px) 0;
  }

  .tree-card {
    --card-radius: 36px;
    position: relative;
    width: min(100%, 680px);
    margin: 0 auto;
    padding: clamp(28px, 5vw, 52px);
    border-radius: var(--card-radius);
    border: 1px solid var(--glass-stroke);
    background:
      linear-gradient(180deg, rgb(255 255 255 / 84%), rgb(248 250 252 / 94%)),
      linear-gradient(135deg, rgb(255 255 255 / 36%), rgb(255 255 255 / 10%));
    box-shadow: var(--shadow-card);
    backdrop-filter: blur(24px);
    text-align: center;
    overflow: hidden;
  }

  .tree-card::before,
  .tree-card::after {
    content: '';
    position: absolute;
    inset: 0;
    pointer-events: none;
  }

  .tree-card::before {
    background:
      radial-gradient(circle at top right, rgb(59 130 246 / 14%), transparent 28%),
      radial-gradient(circle at bottom left, rgb(45 212 191 / 12%), transparent 30%);
  }

  .tree-card::after {
    inset: 1px;
    border-radius: calc(var(--card-radius) - 1px);
    border: 1px solid rgb(255 255 255 / 28%);
    background: linear-gradient(135deg, rgb(255 255 255 / 22%), transparent 30%, rgb(255 255 255 / 10%) 100%);
  }

  .avatar-wrap {
    position: relative;
    width: 104px;
    height: 104px;
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    margin: 0 auto 20px;
    padding: 4px;
    overflow: hidden;
    border: 1px solid rgb(255 255 255 / 64%);
    box-shadow: 0 18px 40px rgb(15 23 42 / 16%);
    background: linear-gradient(145deg, rgb(255 255 255 / 94%), rgb(226 232 240 / 62%));
  }

  .avatar-wrap::after {
    content: '';
    position: absolute;
    inset: -12px;
    z-index: -1;
    border-radius: 50%;
    background: radial-gradient(circle, rgb(96 165 250 / 18%), transparent 65%);
  }

  .avatar-image {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
    border-radius: 50%;
    clip-path: circle(50% at 50% 50%);
  }

  .brand-title {
    position: relative;
    z-index: 1;
    margin: 0;
    color: var(--color-text-primary);
    font-size: clamp(2.4rem, 5vw, 4rem);
    line-height: 0.98;
    letter-spacing: -0.05em;
    font-weight: var(--font-weight-bold);
    margin-top: 0;
  }

  .brand-handle {
    position: relative;
    z-index: 1;
    margin-top: 10px;
    color: var(--color-text-tertiary);
    font-size: 0.92rem;
    font-weight: var(--font-weight-semibold);
    letter-spacing: 0.16em;
    text-transform: uppercase;
  }

  .link-list {
    position: relative;
    z-index: 1;
    margin-top: 28px;
    display: grid;
    gap: 14px;
  }

  .link-btn {
    --button-radius: 20px;
    position: relative;
    min-height: 64px;
    padding: 18px 22px;
    border-radius: var(--button-radius);
    border: 1px solid rgb(255 255 255 / 22%);
    color: var(--lvrs-accent-white);
    font-size: var(--font-description);
    font-weight: var(--font-weight-semibold);
    line-height: 1.35;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    box-shadow: var(--shadow-button);
    overflow: hidden;
    transition:
      transform 220ms ease,
      box-shadow 220ms ease,
      border-color 220ms ease;
  }

  .link-btn::before,
  .link-btn::after {
    content: '';
    position: absolute;
    inset: 0;
    pointer-events: none;
  }

  .link-btn::before {
    inset: 1px;
    border-radius: calc(var(--button-radius) - 1px);
    background: linear-gradient(135deg, rgb(255 255 255 / 20%), transparent 32%, rgb(255 255 255 / 10%) 100%);
  }

  .link-btn::after {
    top: -30%;
    bottom: -30%;
    left: -120%;
    right: auto;
    width: 42%;
    background: linear-gradient(90deg, transparent, rgb(255 255 255 / 38%), transparent);
    transform: rotate(18deg);
    opacity: 0;
  }

  .link-btn.ssprimary {
    background: linear-gradient(135deg, #0f766e, #22c55e 58%, #4ade80 100%);
  }

  .link-btn.ssprimary:hover {
    box-shadow: 0 18px 34px rgb(34 197 94 / 30%);
  }

  .link-btn.ytprimary {
    background: linear-gradient(135deg, #b91c1c, #ef4444 58%, #fb7185 100%);
  }

  .link-btn.ytprimary:hover {
    box-shadow: 0 18px 34px rgb(239 68 68 / 30%);
  }

  .link-btn.blprimary {
    background: linear-gradient(135deg, #16a34a, #22c55e 52%, #86efac 100%);
  }

  .link-btn.blprimary:hover {
    box-shadow: 0 18px 34px rgb(34 197 94 / 24%);
  }

  .link-btn:hover {
    transform: translateY(-3px);
  }

  .link-btn:hover::after {
    opacity: 1;
    animation: sheen 900ms ease;
  }

  .link-btn:focus-visible {
    outline: 3px solid rgb(37 99 235 / 18%);
    outline-offset: 3px;
  }

  @keyframes sheen {
    from {
      transform: translateX(0) rotate(18deg);
    }

    to {
      transform: translateX(520%) rotate(18deg);
    }
  }

  @media (max-width: 640px) {
    .tree-card {
      --card-radius: 28px;
      padding: 24px 20px;
    }

    .avatar-wrap {
      width: 92px;
      height: 92px;
      margin-bottom: 18px;
    }

    .brand-title {
      font-size: clamp(2rem, 11vw, 3.25rem);
    }

    .brand-handle {
      font-size: 0.82rem;
      letter-spacing: 0.12em;
    }

    .link-btn {
      --button-radius: 18px;
      min-height: 58px;
      padding: 16px 18px;
    }
  }
</style>
