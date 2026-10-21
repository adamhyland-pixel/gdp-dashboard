# Agent guide — GDP Dashboard

This is a **public Streamlit GDP learning/dashboard repository**. Do not commit company datasets, private/customer records, credentials, tokens, or other confidential files.

## Working approach
1. **Inspect before editing**: read README.md, requirements.txt, streamlit_app.py and the CSV header; identify data shape and year coverage.
2. **State the decision**: describe the specific visual or metric change and its acceptance criteria.
3. **Prototype separately**: for major UI changes, create three genuinely different information-layout directions, not three colour choices. Do not alter the deployed app during exploration.
4. **Use the dashboard-qa skill** in .agents/skills/dashboard-qa/SKILL.md for data and UX edge cases.
5. **Verify numbers independently**: missing GDP, zero GDP, date ranges, country/year lookup, growth formula. An attractive NaN card is still wrong.
6. **Test edge cases**: empty, one, many, extremes, narrow viewport, keyboard and reduced-motion.
7. **Report with evidence**: which checks ran, limitations, fixes, and what remains provisional.

Do not introduce unnecessary frontend frameworks into the Streamlit prototype. Prefer existing libraries.

*Method inspired by Emil Kowalski's public MIT-licensed agent skills at https://github.com/emilkowalski/skills. This is an independently written adaptation, not an official Emil skill.*
