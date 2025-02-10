---
theme: seriph
background: https://cover.sli.dev
class: 'text-center'
info: |
  ## Testing Strategy Presentation
  Learn about effective testing strategies for software development.

  Learn more at [Sli.dev](https://sli.dev)
transition: slide-left
title: Testing Strategy
mdc: true
---

# Testing Strategy

Effective testing strategies for software development

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" flex="~ justify-center items-center gap-2" hover="bg-white bg-opacity-10">
    Press Space for next page <div class="i-carbon:arrow-right inline-block"/>
  </span>
</div>

---

# Why Testing is Important

- Ensures software quality
- Detects bugs early
- Improves performance
- Enhances user satisfaction

---

# Types of Testing

1. **Unit Testing**
   - Tests individual components
   - Fast and reliable

2. **Integration Testing**
   - Tests interactions between components
   - Ensures modules work together

3. **System Testing**
   - Tests the complete system
   - Validates end-to-end scenarios

4. **Acceptance Testing**
   - Validates user requirements
   - Ensures the system meets business needs

---

# Unit Testing

- Focuses on small, isolated parts of the code
- Uses frameworks like Jest, Mocha, or Jasmine
- Example:

```ts {all|2|4|6|all}
import { sum } from './math'

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3)
})

---

# Thanks a lot!!