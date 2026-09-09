# Nikita Khveshchenko

**Frontend Developer**

---

## Contact

* **Phone:** +375336663389
* **Email:** [runny_life@icloud.com](mailto:runny_life@icloud.com)
* **Telegram:** @runny_life
* **Discord:** runny_life
* **GitHub:** [github.com/runny-life](https://github.com/runny-life)
* **Location:** Belarus

---

## About Me

I recently graduated from Synergy University with a degree in Information Systems and Technology. I'm now focused on
frontend development and looking for my first trainee or junior position.

I enjoy building interfaces, turning designs into working websites and figuring out how things work under the hood.
Currently, I'm focusing on JavaScript and TypeScript, while learning React and building projects to improve my practical
skills. I'm comfortable learning independently, solving problems and working consistently towards a goal.

---

## Technical Skills

* **Languages:** JavaScript (ES6+), TypeScript (basic), HTML5, CSS3
* **Frameworks & Libraries:** React (learning), Tailwind CSS (basic)
* **Tools:** Git, GitHub, npm, Vite, Figma (basic)
* **Web:** Responsive Design, Semantic HTML, BEM, REST API (basic), DOM, Fetch API
* **Other:** Async/Await, working with JSON and APIs

---

## Projects

### Tip Calculator App

* Responsive web application for calculating tips and splitting bills
* Built with HTML5, CSS3 and vanilla JavaScript
* Real-time calculations and custom tip input
* Mobile-first approach
* **[GitHub Repository](https://github.com/runny-life/tip-calculator-app)**

### Password Generator

* Password generator built with TypeScript
* Customizable password length and character sets
* TypeScript types used for application logic
* **[GitHub Repository](https://github.com/runny-life/password-generate-app)**

---

## Code Example

### Password Generator — Frontend Mentor

```typescript
import type {CharacterSet, PasswordOptions} from '../types';

const CHARACTER_SETS: Record<CharacterSet, string> = {
  uppercase: 'ABCDEFGHIJKLMNOPQRSTUVWXYZ',
  lowercase: 'abcdefghijklmnopqrstuvwxyz',
  numbers: '0123456789',
  symbols: '!@#$%^&*()_+-=[]{}|;:,.<>?',
};

function getRandomInt(max: number): number {
  const array = new Uint32Array(1);
  crypto.getRandomValues(array);
  return array[0] % max;
}

export function generatePassword(options: PasswordOptions): string {
  const {length, includes} = options;

  if (length === 0 || includes.length === 0) {
    return '';
  }

  const availableChars = includes
    .map((set) => CHARACTER_SETS[set])
    .join('');

  let password = '';

  for (let i = 0; i < length; i++) {
    const randomIndex = getRandomInt(availableChars.length);
    password += availableChars[randomIndex];
  }

  return password;
}
```

---

