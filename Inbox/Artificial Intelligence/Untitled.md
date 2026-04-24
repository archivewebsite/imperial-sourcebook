Build a responsive web feature for a mental math learning system.

The feature should let users browse, learn, and practice a structured mental math curriculum organized by chapters and lessons.

Curriculum structure:

Chapter 0: Quick Tricks
- Instant multiplication by 11
- Squaring two-digit numbers that end in 5
- Multiplying two two-digit numbers with the same first digit and last digits that add up to 10
- Subtraction trick using rounding and correction
- Quickly adding certain number sequences
- Quick division to produce initial decimal digits
- Calculating restaurant tips, especially 15%
- Basics of memorizing numbers
- Determining the day of the week for a given date, introductory/simple version

Chapter 1: Mental Addition and Subtraction
- Left-to-right addition
- Two-digit addition
- Three-digit addition
- Adding three-digit and four-digit numbers
- Left-to-right subtraction
- Two-digit subtraction
- Subtraction by rounding up
- Three-digit subtraction
- Complement techniques to simplify subtraction

Chapter 2: Basic Multiplication
- Multiplying 2-digit × 1-digit numbers
- Multiplication using the split-number method
- Multiplication by rounding up
- Multiplying 3-digit × 1-digit numbers
- Squaring two-digit numbers
- Squaring using the up-and-down method to the nearest round number
- Basic algebra behind multiplication and squaring tricks

Chapter 3: Intermediate Multiplication
- Multiplying 2-digit × 2-digit numbers
- The addition method for two-digit multiplication
- Shortcut for multiplying by 11
- The subtraction method for two-digit multiplication
- The factoring method for two-digit multiplication
- Friendly products
- Creatively choosing a multiplication method
- Squaring three-digit numbers
- Cubing two-digit numbers

Chapter 4: Mental Division
- Division by a one-digit divisor
- Determining the number of digits in the answer before dividing
- Technique for storing the answer using the Rule of Thumb
- Division by a two-digit divisor
- Decimalization: converting fractions into decimals
- Divisibility tests
- Divisibility tests for 2, 3, 4, 5, 6, 7, 8, 9, 11, and 17
- Fraction operations
- Multiplying fractions
- Dividing fractions
- Simplifying fractions
- Adding fractions with the same denominator
- Adding fractions with different denominators
- Subtracting fractions

Chapter 5: Guesstimation
- Estimating sums
- Estimating differences
- Estimating quotients
- Estimating products
- Estimating square roots
- The divide-and-average method for square roots
- Calculating tips quickly
- Calculating taxes quickly
- Calculating interest quickly
- Applying estimation to everyday math

Chapter 6: Pencil-and-Paper Math
- Adding columns of numbers
- Mod sums for checking addition
- Fast subtraction on paper
- Square roots with pencil and paper
- Pencil-and-paper multiplication
- Criss-cross multiplication
- Casting out elevens to check results

Chapter 7: Memorizing Numbers
- Mnemonics for memorizing numbers
- The phonetic code: converting digits into consonant sounds
- Converting numbers into words
- Memorizing long sequences of numbers
- Memorizing dates
- Memorizing phone numbers
- Using mnemonics to support large mental calculations
- Memory magic

Chapter 8: Advanced Multiplication
- Squaring four-digit numbers
- Multiplying 3-digit × 2-digit numbers
- The factoring method for 3-by-2 multiplication
- The addition method for 3-by-2 multiplication
- The subtraction method for 3-by-2 multiplication
- Squaring five-digit numbers
- Multiplying 3-digit × 3-digit numbers
- The factoring method for 3-by-3 multiplication
- The close-together method
- The addition method for 3-by-3 multiplication
- The subtraction method for 3-by-3 multiplication
- The when-all-else-fails method
- Multiplying 5-digit × 5-digit numbers
- Using the phonetic code to store intermediate results in large multiplications

Chapter 9: Mathematical Magic
- Psychic math
- The Magic 1089
- Missing-digit tricks
- Leapfrog addition
- Magic squares
- How to construct a magic square
- Quick cube roots
- Simplified square roots
- The amazing sum
- Determining the day of the week for any date
- Month codes, year codes, and leap-year rules
- Date calculations in the Gregorian calendar

Feature requirements:

1. Create a clean course dashboard.
   - Show all chapters as cards.
   - Each card should display chapter title, lesson count, completion percentage, and difficulty level.
   - Use a modern educational design: clean layout, soft colors, readable typography, and clear progress indicators.

2. Create a chapter page.
   - Display all lessons in that chapter.
   - Each lesson should have a status: locked, available, in progress, or completed.
   - Users should be able to open a lesson.

3. Create a lesson page.
   Each lesson should include:
   - Lesson title
   - Short explanation
   - Step-by-step method
   - Worked examples
   - Practice questions
   - Answer input field
   - Instant feedback
   - Explanation after answering
   - “Next question” button
   - “Mark lesson complete” button

4. Create a practice mode.
   - Users can choose chapter, lesson, difficulty, and number of questions.
   - Generate math questions based on the selected topic.
   - Track correct answers, wrong answers, accuracy, and time spent.
   - Show a results screen at the end.

5. Create a progress system.
   - Track completed lessons.
   - Track total questions answered.
   - Track accuracy per chapter.
   - Show streaks and achievements.
   - Store progress locally for now using localStorage.

6. Create reusable data structures.
   - Store chapters and lessons in a structured array or JSON object.
   - Each lesson should support:
     - id
     - title
     - chapterId
     - difficulty
     - explanation
     - steps
     - examples
     - practiceGeneratorType
     - completionStatus

7. Add sample lesson content for at least these lessons:
   - Instant multiplication by 11
   - Squaring two-digit numbers that end in 5
   - Left-to-right addition
   - Multiplying 2-digit × 1-digit numbers
   - Divisibility tests

8. Make the UI mobile-friendly.
   - Works well on desktop, tablet, and phone.
   - Use responsive cards, collapsible lesson lists, and large answer buttons for mobile.

9. Add gamification.
   - XP points for completing lessons.
   - Badges for milestones.
   - Daily practice streak.
   - Progress bar for each chapter.

10. Use placeholder logic where advanced math generation is not yet implemented, but structure the code so new lesson generators can easily be added later.

Preferred tech stack:
- React
- TypeScript
- Tailwind CSS
- LocalStorage for progress
- Component-based architecture

Build the first working version as a polished prototype. Prioritize clean structure, beautiful UI, and extensibility.