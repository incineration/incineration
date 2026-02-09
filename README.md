
```rust
use std::collections::HashMap;

#[derive(Debug)]
pub struct Developer {
    pub name: String,
    pub languages: Vec<String>,
    pub age: u8,
    pub expert_languages: Vec<&'static str>,
    pub intermediate_languages: Vec<&'static str>,
    pub learning_languages: Vec<&'static str>,
    pub specialities: Vec<&'static str>,
    pub tools: Vec<&'static str>,
    pub machines: HashMap<String, Machine>,
}

#[derive(Debug, Clone)]
pub struct Machine {
    pub name: String,
    pub cpu: String,
    pub ram: String,
    pub gpu: String,
}

impl Developer {
    pub fn new(name: &str) -> Self {
        let mut machines = HashMap::new();
        machines.insert(
            "Windows".into(),
            Machine {
                name: "Gaming PC".into(),
                cpu: "Intel Core i5-13600K — 14C / 20T · 3.5–5.1 GHz".into(),
                ram: "32GB".into(),
                gpu: "RX 7900 XT".into(),
            },
        );

        Self {
            name: name.to_string(),
            languages: vec!["English".into()],
            age: 19,
            expert_languages: vec!["lua"],
            intermediate_languages: vec!["go", "js", "rust", "java", "python", "html", "react"],
            learning_languages: vec!["c", "c++", "c#", "asm", "php"],
            specialities: vec!["web/app reverse engineering"],
            tools: vec!["vscode"],
            machines,
        }
    }
}

fn main() {
    let dev = Developer::new("incineration");
    println!("{:#?}", dev);
}
```

## Skills

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/lua/lua-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" />
</p>
