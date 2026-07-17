
## Takeaways from the Servidae ELK room in Tryhackme

**Platform:** TryHackMe  
**Topic:** Log analysis using Kibana/ELK stack

### Key Lessons

1. **Use queries, don't trust the visuals blindly**
   - Histograms can look like peak activity 
     but clicking them shows nothing useful
   - KQL queries give you actual control 
     over what you're seeing

2. **Please look into the fields properly**
   - Don't just read the top-level summary
   - Expand log entries and check every field
   - The important detail is usually buried
   - also check the top values of a field

3. **Add fields as columns**
   - Makes comparing events WAY easier
   - Instead of expanding every single log,
     you can see patterns across rows instantly
   - Saves so much time during investigation & makes things readable.

### The Histogram takeaway:
Histogram showed what looked like peak 
suspicious activity → clicked it → 
process column was blank → learned to 
just write the query directly instead
of trusting the graph

→ Lesson: graphs help you spot WHERE to look,
  queries help you actually find WHAT is there
```
