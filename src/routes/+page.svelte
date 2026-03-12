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
    <h1>최원준가구갤러리</h1>
    <p>@jun3.3</p>
    <nav class="link-list">
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
    min-height: calc(100vh - 32px);
    margin-bottom: 0;
    align-items: center;
    justify-content: center;
  }

  .tree-card {
    width: 100%;
    max-width: 560px;
    margin: 0 auto;
    padding: clamp(24px, 5vw, 42px);
    border-radius: 32px;
    border: 1px solid var(--color-border-secondary);
    background: var(--color-surface-primary);
    box-shadow: 0 24px 44px var(--lvrs-shadow-strong);
    text-align: center;
  }

  .avatar-wrap {
    width: 80px;
    height: 80px;
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    margin: 0 auto 12px;
    overflow: hidden;
    border: 1px solid var(--color-border-primary);
    box-shadow: 0 10px 20px var(--lvrs-shadow-strong);
    background: var(--color-surface-secondary);
  }

  .avatar-image {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
    border-radius: 50%;
    clip-path: circle(50% at 50% 50%);
  }

  h1 {
    margin: 0;
    color: var(--color-text-primary);
    font-size: var(--font-title2);
    line-height: 1.06;
    font-weight: var(--font-weight-bold);
    margin-top: 32px;
  }

  p {
    color: var(--lvrs-accent-gray);
  }

  .link-list {
    margin-top: 22px;
    display: grid;
    gap: 12px;
  }

  .link-btn {
    min-height: 56px;
    border-radius: 16px;
    border: 1px solid var(--color-border-primary);
    background: var(--color-surface-secondary);
    color: var(--color-text-primary);
    font-size: var(--font-body);
    font-weight: var(--font-weight-semibold);
    display: grid;
    place-items: center;
    transition:
      transform 140ms ease,
      background-color 140ms ease,
      border-color 140ms ease;
  }

  .link-btn.ssprimary {
    color: var(--lvrs-accent-white);
    border-color: var(--lvrs-accent-transparent);
    background: linear-gradient(
      145deg,
      var(--lvrs-accent-base-teal),
      var(--lvrs-accent-dim-green-vivid)
    );
  }

  .link-btn.ssprimary:hover {
    background: linear-gradient(
      145deg,
      var(--lvrs-accent-base-teal),
      var(--lvrs-accent-base-green-vivid)
    );
  }

  .link-btn.ytprimary {
    color: var(--lvrs-accent-white);
    border-color: var(--lvrs-accent-transparent);
    background: linear-gradient(
      145deg,
      var(--lvrs-accent-base-red-vivid),
      var(--lvrs-accent-dim-red)
    );
  }

  .link-btn.ytprimary:hover {
    background: linear-gradient(
      145deg,
      var(--lvrs-accent-dim-red),
      var(--lvrs-accent-base-red-birch)
    );
  }

  .link-btn.blprimary {
    color: var(--lvrs-accent-white);
    border-color: var(--lvrs-accent-transparent);
    background: linear-gradient(
            145deg,
            var(--lvrs-success),
            var(--lvrs-accent-light-green)
    );
  }

  .link-btn.blprimary:hover {
    background: linear-gradient(
            145deg,
            var(--lvrs-accent-base-teal),
            var(--lvrs-accent-dim-green-vivid)
    );
  }

  @media (max-width: 640px) {
    h1 {
      font-size: var(--font-title);
    }
  }
</style>
