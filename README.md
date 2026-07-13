import profile from "./data/profile";

function App() {
  return (
    <div>
      <h1>Hi there I'm {kavinn}</h1>
      <h2>{profile.title}</h2>

      <ul>
        <li>{profile.about.education}</li>
        <li>{profile.about.description}</li>
        <li>{profile.about.learning}</li>
        <li>{profile.about.hobby}</li>
      </ul>

      <blockquote>
        "{profile.quote.text}"
        <br />
        — {profile.quote.author}
      </blockquote>

      <div>
        {profile.socials.map((social) => (
          <a
            key={social.name}
            href={social.url}
            target="_blank"
            rel="noopener noreferrer"
          >
            {social.name}
          </a>
        ))}
      </div>
    </div>
  );
}
