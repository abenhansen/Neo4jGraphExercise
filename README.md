## Neo4J

1. CREATE (mm:Movie {title:"Forrest Gump"})
2.  MATCH(mm {title: "Forrest Gump"})
    SET mm.released = 1995, mm.tagline = " Life is like a box of chocolates...you never know what you’re gonna get" 
    return mm.title, mm.released, mm.tagline
    
3. MATCH(mm {title: "Forrest Gump"})
   SET mm.released = 1994
   return mm.title, mm.released, mm.tagline
   
4. MATCH(mm {tagline: "Free your mind"})
   return mm.title, mm.released, mm.tagline
   
5. MATCH(mm {title: "The Matrix"})-[r]-(c)
   return r
   
6. MATCH(mm {title: "The Matrix"})<-[r]-(people)
   return people.name, type(r)

7. MATCH(people)
   WHERE people.born < 2000
   return people
   
 8. MATCH(mm {title: "The Da Vinci Code"})<-[r:REVIEWED]-(people) 
    where r.rating > 65
    return people.name, r
    
 9. MATCH(a {name:"Angela Scope"})<-[r:FOLLOWS]->(followers) 
    return followers.name
  
  10. MATCH(a {name:"Jessica Thompson"})<-[r:FOLLOWS]-(followers) 
      return followers
      
  11. Helped doesnt exist as a propety on any relation in the movie DB?
      
  12. Helped doesnt exist as a propety on any relation in the movie DB?
   
"# Neo4jGraphExercise" 
