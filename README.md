# omar-bakry-website007
import React, { useState } from 'react';

const App = () => {
  const [activeTab, setActiveTab] = useState('about');

  const showTab = (tabId) => {
    setActiveTab(tabId);
  };

  return (
    <div style={{ fontFamily: 'Segoe UI, Tahoma, Geneva, Verdana, sans-serif', background: 'linear-gradient(to right, #f7cac9, #ffffff, #88b04b)', color: '#2e2e2e', fontSize: '1.25rem' }}>
      <header style={{ textAlign: 'center', padding: '2rem 1rem' }}>
        <h1 style={{ fontSize: '3rem', color: '#6b5b95' }}>Omar Bakry | English 210 E-Portfolio</h1>
        <h2 style={{ fontSize: '2rem', color: '#ff6f61' }}>Guided by Professor Anne Schmalstig</h2>
      </header>

      <nav style={{ display: 'flex', justifyContent: 'center', gap: '1rem', padding: '1rem', backgroundColor: '#ffcccb', borderRadius: '12px', margin: '0 1rem 2rem' }}>
        {['about', 'presentation', 'video', 'complaint'].map(tab => (
          <button
            key={tab}
            onClick={() => showTab(tab)}
            className={activeTab === tab ? 'active' : ''}
            style={{ background: activeTab === tab ? '#3c1361' : '#6b5b95', color: 'white', border: 'none', padding: '0.75rem 1.25rem', borderRadius: '8px', cursor: 'pointer', fontWeight: 'bold' }}
          >
            {tab === 'about' ? 'E-Portfolio' : tab.charAt(0).toUpperCase() + tab.slice(1).replace(/([A-Z])/g, ' $1')}
          </button>
        ))}
      </nav>

      {activeTab === 'about' && (
        <section style={sectionStyle}>
          <h2 style={h2Style}>About Me</h2>
          <p>
            My name is <strong>Omar Bakry</strong>, a third-year Electrical and Computer Engineering student at <strong>Texas A&M University</strong>.
            I'm passionate about solving real-world problems through technology. Outside academics, I enjoy football, reading, and the gym.
          </p>
          <p>
            This portfolio is a culmination of everything I’ve learned and created in <strong>English 210</strong>, taught by the incredible Professor Anne Schmalstig. It includes my <strong>resume</strong>, <strong>cover letter</strong>, collaborative work with peers, and professional writing samples.
          </p>
          <p>
            My team—<strong>Mohammed Mutlaq</strong>, <strong>Rashid</strong>, <strong>Amer</strong>, and <strong>Issa</strong>—worked closely together this semester. We brainstormed ideas, supported each other through challenges, and celebrated our progress as a team.
          </p>
          <img src="https://cdn.pixabay.com/photo/2014/04/02/10/55/teamwork-307838_960_720.png" alt="Teamwork Cartoon" style={imgStyle} />
        </section>
      )}

      {activeTab === 'presentation' && (
        <section style={sectionStyle}>
          <h2 style={h2Style}>Electric Cars Presentation</h2>
          <p>
            Our group created a presentation focused on <strong>electric vehicles</strong>, especially their braking systems. We examined how regenerative braking works and the safety challenges that come with it.
          </p>
          <p>
            Everyone had a task: some of us researched, others designed slides, and I personally worked on delivering part of the content. We practiced as a group multiple times to ensure a smooth delivery.
          </p>
          <img src="https://cdn.pixabay.com/photo/2022/10/10/08/50/electric-car-7509857_960_720.jpg" alt="Electric Car Cartoon" style={imgStyle} />
        </section>
      )}

      {activeTab === 'video' && (
        <section style={sectionStyle}>
          <h2 style={h2Style}>Video Project</h2>
          <p>
            In our second major assignment, we developed a <strong>video project</strong> on electric car braking issues. We used AI tools, added effects, and wrote a compelling script to raise awareness about technical flaws.
          </p>
          <p>
            I played a leading role in editing, animating, and finalizing the video. Our teamwork allowed us to produce something we’re truly proud of. It’s both educational and entertaining!
          </p>
          <img src="https://cdn.pixabay.com/photo/2016/04/24/20/51/youtube-1359713_960_720.png" alt="Video Project Cartoon" style={imgStyle} />
        </section>
      )}

      {activeTab === 'complaint' && (
        <section style={sectionStyle}>
          <h2 style={h2Style}>Letter of Complaint</h2>
          <p>
            For our last major task, we crafted a <strong>letter of complaint</strong> directed at authorities in Qatar. Our concern was the slow EV charging speeds. We approached the issue respectfully and requested feedback.
          </p>
          <p>
            This experience taught us how to communicate grievances professionally and respectfully. We also developed our persuasive writing skills.
          </p>
          <img src="https://cdn.pixabay.com/photo/2020/08/28/20/53/man-5524788_960_720.png" alt="Letter Cartoon" style={imgStyle} />
        </section>
      )}

      <footer style={{ textAlign: 'center', marginTop: '4rem', padding: '2rem', color: '#6b5b95' }}>
        <p>© 2025 Omar Bakry | Texas A&M University | English 210 | Professor Anne Schmalstig</p>
      </footer>
    </div>
  );
};

const sectionStyle = {
  padding: '2rem',
  maxWidth: '1000px',
  margin: '0 auto',
  background: '#ffffff',
  borderRadius: '20px',
  boxShadow: '0 4px 16px rgba(0, 0, 0, 0.2)'
};

const h2Style = {
  fontSize: '2rem',
  color: '#ff6f61'
};

const imgStyle = {
  maxWidth: '100%',
  borderRadius: '10px',
  marginTop: '1rem',
  boxShadow: '0 2px 8px rgba(0, 0, 0, 0.1)'
};

export default App;
