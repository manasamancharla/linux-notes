# Vim

[Reference](https://www.linuxfoundation.org/blog/blog/classic-sysadmin-vim-101-a-beginners-guide-to-vim)

## The Modes
- **Command Mode** (default) – Used for navigation and command execution.
- **Insert Mode** – Used for text editing (press `i` to enter, `Esc` to exit).
- **Last Line Mode** – Used for saving, quitting, and searching (press `:` in Command mode).

---
### Plain Text to practise

The United States of America is a federal republic located primarily in North America.
It is commonly referred to as the United States, the U.S., or simply America.
The country consists of 50 states, a federal district, and several territories.
The capital city of the United States is Washington, D.C.
The largest city by population is New York City.

The United States declared independence from Great Britain on July 4, 1776.
This declaration was written primarily by Thomas Jefferson.
The American Revolutionary War followed the declaration of independence.
The war ended in 1783 with the Treaty of Paris.
After independence, the U.S. formed a new government under the Constitution.

The United States Constitution was adopted in 1787.
It is one of the oldest written constitutions still in use.
The Constitution establishes three branches of government.
These branches are the legislative, executive, and judicial branches.
The system is designed to provide checks and balances.

The legislative branch is represented by Congress.
Congress is divided into the Senate and the House of Representatives.
The executive branch is led by the President.
The judicial branch is headed by the Supreme Court.
This structure ensures no single branch becomes too powerful.

The United States has a diverse population.
It is often described as a nation of immigrants.
People from around the world have moved to the U.S. over centuries.
This diversity has shaped American culture.
American culture blends influences from Europe, Africa, Asia, and Latin America.

The U.S. economy is one of the largest in the world.
It is driven by industries such as technology, finance, healthcare, and manufacturing.
Major technology companies are based in Silicon Valley, California.
Wall Street in New York City is a global financial center.
The U.S. dollar is one of the world's primary reserve currencies.

Geographically, the United States is vast and varied.
It includes mountains, deserts, forests, and coastlines.
The Rocky Mountains run through the western part of the country.
The Appalachian Mountains are located in the east.
The Great Plains stretch across the central region.

The Mississippi River is one of the longest rivers in North America.
The Grand Canyon in Arizona is a famous natural landmark.
Yellowstone National Park was the first national park in the world.
The United States has a wide range of climates.
Climate ranges from Arctic conditions in Alaska to tropical weather in Florida and Hawaii.

The country operates under a federal system.
Each state has its own government.
States have authority over education, transportation, and local laws.
However, federal law overrides state law when conflicts arise.
This balance defines American federalism.

Education in the United States includes public and private institutions.
There are thousands of universities and colleges.
Some globally recognized institutions include Harvard University and MIT.
Public education is managed at the state and local level.
Higher education attracts students from around the world.

The United States military is one of the most powerful in the world.
It consists of the Army, Navy, Air Force, Marine Corps, and Space Force.
The President serves as Commander-in-Chief.
The U.S. maintains military bases in several countries.
Defense spending is a significant part of the federal budget.

American political life is often dominated by two major parties.
These are the Democratic Party and the Republican Party.
Elections are held regularly at federal, state, and local levels.
Presidential elections occur every four years.
Citizens over the age of 18 are eligible to vote.

The United States has a strong tradition of free speech.
The First Amendment protects freedom of religion and expression.
The Bill of Rights outlines fundamental civil liberties.
The Supreme Court interprets constitutional issues.
Court decisions can significantly shape national policy.

The U.S. played a major role in both World Wars.
After World War II, it emerged as a global superpower.
It was a founding member of the United Nations.
The Cold War defined much of its foreign policy in the 20th century.
Today, it remains influential in global affairs.

Culturally, the United States has a major global influence.
Hollywood is a leading center of the film industry.
American music genres include jazz, blues, rock, and hip-hop.
Sports such as American football, basketball, and baseball are popular.
The Super Bowl is one of the most watched sporting events in the country.

The country is known for technological innovation.
The internet was developed with significant American involvement.
NASA leads major space exploration missions.
The Apollo 11 mission landed the first humans on the Moon in 1969.
Space exploration continues to be a national priority.

Transportation infrastructure includes highways, railroads, and airports.
The Interstate Highway System connects major cities.
Air travel is widely used for long-distance transportation.
Major airports include Atlanta, Los Angeles, and Chicago.
Public transportation systems vary by city.

The United States faces ongoing challenges.
These include economic inequality, healthcare access, and climate change.
Debates over immigration policy are common.
Political polarization has increased in recent years.
Despite challenges, democratic institutions continue to function.

The national flag consists of 13 stripes and 50 stars.
The stripes represent the original 13 colonies.
The stars represent the 50 states.
The national anthem is "The Star-Spangled Banner."
The bald eagle is a national symbol.

The United States continues to evolve socially and politically.
Innovation, diversity, and debate are central to its identity.
It remains one of the most studied and discussed countries in the world.
Its influence spans economics, culture, science, and politics.
The story of the United States is still being written.

---

### Basic Navigation
- `0` – Move to the **beginning** of the line  
- `$` – Move to the **end** of the line  
- `w` – Move to the **next word**  
- `b` – Move to the **previous word**  
- `gg` – Move to the **start** of the file  
- `G` – Move to the **end** of the file  
- `:n` – Move to **line number `n`**  
- `` `. `` – Move to the last edit position 

---
### Editing Text
- `dw` – Delete a **word**  
- `dd` – Delete a **line**  
- `d$` – Delete from **cursor to end of line**  
- `d0` – Delete from **cursor to beginning of line**  
- `D` – Delete from **cursor to end of line**  
- `u` – **Undo** last action  
- `Ctrl + r` – **Redo** an undone change
- `x` – Delete a **character**  
- `X` – Delete a **character before cursor**    

---

### Insert Mode
- `i` – Insert before cursor  
- `Esc` – Exit insert mode  

---
### Searching And Replacing
- `/pattern` – Search **forward** for a pattern  
- `?pattern` – Search **backward** for a pattern  
- `n` – Move the cursor to the next instance of the text from the last search  
- `N` – Move the cursor to the previous instance of the text from the last search
- `:%s/old/new/g` – Replace **all occurrences** of "old" with "new"  
- `:s/old/new/g` – Replace **all occurrences** in the current line  

---
### Copying And Pasting
- `v` – Highlight one character at a time  
- `V` – Highlight one line at a time  
- `Ctrl-v ` – Highlight by columns 
- ` y ` - Yank text into the copy buffer
- `yy` – Copy (yank) a **line**  
- `yw` – Copy (yank) a **word**  
- `p` – Paste text **after** the current line  
- `P` – Paste text **on** the current line  

---
### Saving and Quitting
- `:w` – Write the file to the existing filename  
- `:w filename` – Write the file to the different filename  
- `:q` – Quit
- `:q!` – Quit without saving changes
- `:wq` – Save and quit 











