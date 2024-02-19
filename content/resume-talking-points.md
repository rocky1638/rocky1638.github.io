# Resume Talking Points

## Experiences.

### Software Engineer @ Meta.

**Technologies:** Javascript/React/React Native, PHP/Hack, GraphQL, C++.

> Improved internal meeting workflows for >80000 employees by implementing screenshare pausing functionality in Messenger Video Calls using React Native and C++, which was released internally.

- Allowed the desktop version of Messenger to pause screenshares.
- **React Native** implementation on the frontend, which communicated with a C++ backend through gRPC.
- Simple use case to **make it easier to stop screenshares** when screen-sharer wanted to temporarily hide their screen, instead of having to
- Screensharing was implemented by sending screenshots consistently at some framerate.
	- The actual implementation was **implemented by storing the last frame before the screenshare was paused**, and this last screen was just constantly sent until the screenshare was unpaused.

> Streamlined internal privacy review process by creating functionality in PHP, React, and GraphQL to allow privacy managers to update linked privacy tasks directly.

- React/Javascript/Typescript implementation on the frontend with GraphQL, PHP/Hack backend.
- **The Launch Manager tool allowed employees who were “launch managers” to see the status of and edit settings of privacy reviews**, which were mandatory reviews that were conducted on new features to ensure that they comply with all privacy rules.
- There were internal tasks created for these privacy reviews, and internal customers wanted a way to be **able to update the linked task on a privacy review**, which was not currently available.

#### Challenges.

- Testing environment especially at a big company.
- Navigating the backend C++ code, and figuring out how it was communicating with Redux in the frontend.
- Design decision concerning UX when it came to having users press a button vs. auto-updating the linked task after it was selected in the autocomplete-selection bar.

#### Impact.

- Increase the efficiency of fellow Meta employees.
	- Added in a functionality that previously needed to be given to devs/someone with technical experience to manually query the data to update.
	- No longer need to stop screensharing and restart when something needs to be hidden on screen.

### Software Engineer Intern @ Tesla.

**Technologies:** Javascript/React, GraphQL/Apollo, Python.

> Improved efficiency of part inspection and production line error analysis for engineers and technicians by over 50% by developing an all-in-one internal platform in React and GraphQL.

- Design engineers originally tracked part shipments and inspection results in an Excel spreadsheet.
- Worked on a full-stack application that **provided a dashboard to show design engineers the inspection results of various parts on the production line.**
	- The application showed:
		- Whether a specific part had passed or failed inspection, and camera images from the inspection line.
		- Aggregate by type of part, and see failure rates.
		- Allow searching and filtering through parts by various properties.
	- **Inspection was done by machine learning segmentation models on separate backend services** that I did not work on, but used the results from.

> Cut average factory error response time in factory by 30% by consolidating quality control problems across all production lines and creating a technician notification center.

- On the same app, we had a backend job that would run daily to generate notifications for new part types that were failing more than normal.
	- Done by looking through new part inspections in the database and aggregating data to see failure rates on the day compared to historical failure rates, by a threshold.
- Display this in a notification center screen on the front-end app.

> Improved specificity of security across internal apps by implementing keyword and role based permissioning using AWS Lambdas.

- Updated **authentication and permissioning** throughout the internal tools app to use **arrays of keywords instead of a single keyword**, to allow for more flexibility when comparing the roles of a user with the allowed roles for an endpoint or resource.
- The code for this authentication service was deployed and ran on AWS Lambdas.

#### Challenges.

- Updating React state and improving efficiency of React app using native Apollo state as well as new React hooks such as `useEffect` and `useMemo`.
- Various front-end challenges with styling, responsive design.

#### Impact.

- Improved efficiency of iteration process for design engineers at Tesla, reducing the overhead to improving the car designs.
	- The overhead was having to figure out which parts needed to be looked at closer/reworked.
	- Now, they could just easily find these parts through an easy-to-use web app, and be notified if any parts were failing inspection more than usual.

### Software Engineer Intern @ StackAdapt.

**Technologies:** Javascript/React, Ruby on Rails.

> Expanded potential client access to more than 150 million users on Spotify and SoundCloud by building out targeted audio ad campaign functionality in Ruby on Rails and React.

- Added features in a fullstack web application on a React/Typescript frontend and a Ruby on Rails backend.
- Worked on adding functionality to the ad campaign creator/editor, allowing business users to specify audio files and platforms to advertise their audio files on, including Spotify and SoundCloud.
- Mostly focused on the frontend functionality.

> Created a master demo account environment to enhance sales team workflows and improve customer acquisition success, helping to achieve 1000 active ad campaigns.

- Worked with database seeding and migrations to create custom demo account for the business to try to recruit more clients to the platform.
- Did manual and integrated testing to ensure that the demo platform performed as expected, and worked with the business team to figure out the requirements for the account.

> Upgraded capabilities of ad campaign editor to allow for bulk editing, saving customers up to 2 hours per day

- This was more full-stack work on the business-client facing product, which allowed customers to bulk edit multiple campaigns at once to switch out media, change targeting keywords, etc.
- Heavily improved the workflow of some campaign managers, as many teams had tens of campaigns running at once and it was a large hassle to try and update a small value on all of them.
- Also updated routes on the backend to be able to take the option of updating multiple campaign values at once.

#### Challenges.

- Making sure performance was good on the frontend, because we had a very large form that held a lot of Redux state at any given time.
	- Tried to make sure to not update any components unless necessary, using `useMemo` to make sure components were memoized and weren’t rerendered with every input.
- Working back and forth with business team to finalize requirements of the demo account, and dealing with changing requirements.
	- Made sure to keep communication open, and update them each time I changed anything to get live reactions and feedback.

#### Impact.

- Enabled business clients to access a previously inaccessible pool of users from audio platforms.
- Improved the efficiency and consistency of sales team members, as they no longer had to maintain a normal user account and make sure that it had the correct data; they could instead use an account that would start from the exact same state each time.

### Software Engineer Intern @ KitchenMate.

**Technologies:** Javascript/AngularJS, Ruby on Rails, SQL, Python/Jupyter, Figma.

> Increased projected revenue by 30% by expanding customer base to hospitals, through scoping out and building a full-fledged concierge app experience.

- The original experience was a self-serve experience where employees use their phones to pick out a meal and cook it.
	- They would pay through the app.
- For hospitals, patients and family members were often preoccupied in their rooms, so another experience was created to allow patients to create orders for meals, and to allow nurses or hospital workers to cook the meals and deliver it to their rooms.
- Full-stack task including AngularJS frontend and Ruby on Rails backend.

> Created an internal asset management tool using AngularJS, streamlining operations processes and saving 10 total hours weekly.

- Rich text notes.
- Internal asset management system for everything from refrigerators to smart cookers, showing status of the cooker, location, recent maintenance notes, etc.
- Allowed the operations team a central place to look for all the necessary information about a piece of hardware when servicing was needed to be done.

> Streamlined weekly inventory planning process by architecting and optimizing an inventory prediction model using TensorFlow/Keras.

- Attempted to use a neural network to predict the number of each menu item should be sent to each location based on various features such as:
	- Number of employees at a location.
	- Distribution of vegans, vegetarians, etc.
	- Historical amount of meals sent/eaten by week at the location.
	- Weather, other environmental factors.

> Boosted weekly average users by 5% by implementing a C2C2B referral program.

- Implemented a referral program by generating referral keys in the backend, and creating banners and a dedicated referral page in the frontend.
- Allowed new users to access the signin page with a referral, and recorded new users with the person who referred them in the database.

> Decreased weekly food waste by 10% with a historical analysis tool in Jupyter Notebooks to evaluate inventory prediction scripts.

- Used a fairly manual approach in a Python notebook to create weekly menus based on a set of requirements dictated by the culinary team.
	- These requirements included the minimum number of vegan/vegetarian items, whether a certain menu item was on the menu last week, etc.
- Exported these menus to a Google sheets file that could be viewed by the food production team, as well as created a database transaction that showed the menu in the actual internal ops app.

> Lead entire application redesign and styleguide creation in Figma, working with marketing and business teams.

- Pretty self-explanatory, worked with business team and handed it off when I left.

#### Challenges.

- Learning AngularJS when all I had seen before was React.
- Making an efficient prediction algorithm with Python when having to implement so many functional requirements, and working with the culinary team.

#### Impact.

- Referral program and concierge experience for hospitals increased revenue and users substantially.
- Rich text notes and ability to track physical items necessary for operation was extremely useful for the operations team, and saved a lot of time weekly.

### Fullstack Developer Intern @ ConsenSys.

**Technologies:** Javascript/React, Apollo/GraphQL, Node/Express.

> Bolstered frontend test coverage by 20% with Jest snapshot and pixel-match tests.

- Used Jest to perform snapshot testing and React component testing.

> Built [[clean-architecture]] endpoints over existing Node/Express API, allowing for framework-agnostic business logic and increasing developer efficiency.

- Refactored the API to separate entities and business-logic away from framework logic such as Express.
	- The Express endpoints simply called a controller that called a usecase *(with all the business logic)*.
	- The usecase contained the business logic, and dealt with entities that contained logic that was mapped to the data model on the database.

## Side Projects.

![[eeg-seizure-detection]]
