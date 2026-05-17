<template>
  <main class="home">
    <section class="poster">
      <header class="top-row">
        <div class="brand">
          <p>Custom build.</p>
          <p>Hack the future.</p>
        </div>
        <button class="future-btn">Future &gt;&gt;&gt;</button>
      </header>

      <div class="content-grid">
        <article class="left-panel panel">
          <div class="planet-block frame">
            <div class="planet"></div>
            <div class="tagline">Drive beyond the horizon—where past meets future</div>
          </div>
          <h2 class="delorean-title">DELOREAN</h2>
          <div class="small-monitor frame">
            <div class="monitor-screen"></div>
            <div class="monitor-bars">
              <span v-for="i in 6" :key="`bar-${i}`"></span>
            </div>
          </div>
        </article>

        <article class="right-panel panel">
          <h1 class="main-title">CYBER<br />DRIVE</h1>
          <div class="signal-line"></div>
          <div class="car-card frame">
            <div class="card-head">
              <span>Delorean</span>
              <span>Run</span>
            </div>
            <div class="saturn"></div>
            <div class="car-shape"></div>
          </div>
        </article>
      </div>

      <footer class="bottom-row frame">
        <div class="data-card">
          <h3>DATA CARD</h3>
          <div class="data-info">
            <span>TYPE</span>
            <span>NAME</span>
            <span>CAR</span>
            <span>1985</span>
          </div>
        </div>
        <div class="pixel-code"></div>
      </footer>
    </section>
  </main>
</template>

<style scoped>
.home {
  min-height: 100vh;
  padding: 1.2rem;
  background: #09090d;
  color: #e9ddcf;
  font-family: "Courier New", "Lucida Console", monospace;
}

.poster {
  max-width: 980px;
  margin: 0 auto;
  border: 2px solid #6f95ca;
  background: radial-gradient(circle at 50% 20%, #1b202b 0%, #09090d 58%);
  padding: 1rem;
  box-shadow: 0 0 24px rgba(115, 159, 224, 0.18);
}

.top-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 1rem;
  font-size: 0.8rem;
  color: #8eaed8;
}

.brand p {
  margin: 0;
}

.future-btn {
  border: 1px solid #6f95ca;
  background: transparent;
  color: #8eaed8;
  font: inherit;
  padding: 0.2rem 0.6rem;
}

.content-grid {
  display: grid;
  grid-template-columns: 1fr 1.6fr;
  gap: 1rem;
}

.panel {
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
}

.frame {
  border: 2px solid #6f95ca;
  background: #0d1118;
}

.planet-block {
  padding: 0.8rem;
}

.planet {
  width: 100%;
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  margin: 0 auto 0.8rem;
  background: radial-gradient(circle at 30% 30%, #f4e8db 0%, #e8ddcf 36%, #1d2331 37%, #09090d 100%);
  box-shadow: inset -22px -18px 0 #09090d;
}

.tagline {
  background: #7ba1d8;
  color: #0c111b;
  padding: 0.7rem;
  font-weight: 700;
  line-height: 1.15;
}

.delorean-title {
  margin: 0;
  font-size: clamp(2rem, 4vw, 3.2rem);
  letter-spacing: 0.1em;
  color: #7ba1d8;
}

.small-monitor {
  padding: 0.6rem;
}

.monitor-screen {
  height: 68px;
  margin-bottom: 0.55rem;
  background: linear-gradient(135deg, #212837 0%, #5f7ca6 45%, #11151d 100%);
}

.monitor-bars {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 0.35rem;
}

.monitor-bars span {
  height: 8px;
  border: 1px solid #6f95ca;
}

.main-title {
  margin: 0;
  font-size: clamp(3rem, 11vw, 6.5rem);
  line-height: 0.9;
  letter-spacing: 0.06em;
  color: #7ba1d8;
}

.signal-line {
  height: 18px;
  border: 2px solid #6f95ca;
  background: repeating-linear-gradient(
    90deg,
    #7ba1d8 0 6px,
    #0d1118 6px 8px,
    #7ba1d8 8px 12px,
    #0d1118 12px 16px
  );
}

.car-card {
  padding: 0.7rem;
}

.card-head {
  display: flex;
  justify-content: space-between;
  color: #7ba1d8;
  margin-bottom: 0.7rem;
}

.saturn {
  width: 42%;
  aspect-ratio: 1/1;
  border-radius: 50%;
  margin: 0 auto 1rem;
  background: #7ba1d8;
  position: relative;
}

.saturn::after {
  content: "";
  position: absolute;
  top: 45%;
  left: -25%;
  width: 150%;
  height: 26%;
  border: 2px solid #7ba1d8;
  border-radius: 999px;
}

.car-shape {
  height: 180px;
  background:
    linear-gradient(#f4e8db 0 64%, transparent 64%),
    linear-gradient(135deg, transparent 8%, #f4e8db 10% 72%, transparent 74%),
    linear-gradient(90deg, #f4e8db 0 100%);
  clip-path: polygon(6% 52%, 20% 35%, 50% 28%, 75% 33%, 92% 45%, 98% 63%, 93% 76%, 9% 76%);
}

.bottom-row {
  margin-top: 1rem;
  padding: 0.7rem;
  display: grid;
  grid-template-columns: 1.2fr 2fr;
  gap: 0.8rem;
}

.data-card h3 {
  margin: 0 0 0.45rem;
  font-size: 1.85rem;
  color: #e9ddcf;
}

.data-info {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.25rem 0.6rem;
  color: #7ba1d8;
  font-size: 0.78rem;
}

.pixel-code {
  border: 2px solid #6f95ca;
  background:
    radial-gradient(circle at 20% 30%, #7ba1d8 8%, transparent 9%) 0 0 / 24px 24px,
    radial-gradient(circle at 66% 72%, #7ba1d8 8%, transparent 9%) 0 0 / 24px 24px,
    #0d1118;
}

@media (max-width: 860px) {
  .content-grid,
  .bottom-row {
    grid-template-columns: 1fr;
  }

  .main-title {
    font-size: clamp(2.7rem, 18vw, 5rem);
  }
}
</style>
