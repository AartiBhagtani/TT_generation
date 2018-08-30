## TT_generation  
### To build a automatic timetable generator system department wise for KJ somaiya college.


#### To generate a timetable following resources are  required for lecture-
 
  Day n Time Slots( fixed. Here, Monday - friday, 9 - 5)
  Teacher
  Classroom
  Subject (and labs)

Last 3 resources are taken from user.

### Algorithm
It consists of 4 essential steps
#### Population Selection:
  Each population set consists of chromosomes of 
  Subjects - It consists of subjects for each year and division, with its corresponding teacher.
  Thus it consists of subject name, teacher id, day, timeslot.

  Labs - Similar to subjects it consists of labs for every year and division. As there are 4 batches for a particular year and division, at a time 4 labs are picked.

  These chromosomes are generated for random day and time slot for each and every subjects and labs. The no of chromosomes depends on the population size of subjects and labs. 

  Calculation of conflicts - there can be 2 types of conflicts
  Teacher conflict - when same teacher teaches in 2 different class(lab) for a particular time slot.
  Room conflict - when same room is occupied by 2 different classes at a time.

  Possibilities of conflicts in this case:
  Teacher conflict between 2 labs
  Teacher conflict between 2 theory subject 
  Room conflict for labs and theory subjects
  Teacher conflict between between lab and theory subject.
  Thus to calculate no of conflicts the algorithm is

  for a particular day and time slot {
       Increase conflict by 1 if any of the above        cases.
  }

#### Cross over - 
  In crossover the resources like rooms, teachers, subjects are exchanged(crossovered) in population.

#### Mutation - 
  To add more variations to population resources are also exchanged from whole pool of resources.

#### Conflict free - Time table generation.
  For each division, day, time slot conflict free is lecture. Thus, complete timetable is created.

##### Frozen constraints  
Lectures like p2, zero hour, T&P.


Tech stack used:
  Python 3.x
  Flask
  Genetic Algorithm


