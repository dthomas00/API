This is the sum of the API testing exercises. There are several Word files, an Excel document, and two JSON files that contain the actual API tests with GitHub. I'll go into each individually below.


Exercise A - This is a document explaining my concerns about testing the GitHub API, what areas I think would be difficult to test, what I would focus on etc. It is fairly short and to the point.

Exercise B - This is a document explaining in detail how I would go about testing the GitHub API, as well as some detail about which tests I would automate and why, and which tests I would leave to manual testing.

Exercise C - This is a very simple test plan of the GitHub API, it covers the vast majority of the API in question. It also contains the test scenarios for the facebook/react/issues, and facebook/react/issues8850 endpoint. The test plan is pretty large, but it is very basic, I just worked on getting the foundation of the plan - making sure the API endpoints work, it would take another detailed pass for the test plan to really get filled out. If more needs to be added, I can certainly do that, but I think this is a very good start.

Exercise D - There are two JSON files in the repository that contain the actual tests for the issues, and issues 8850 endpoints. I used an open source program called Postman which allows one to easily create modular API tests that can be easily shared with other Postman users. All you need to do to run the tests is download and install Postman, download the JSON files, then import them into the collections section of Postman and run. There are a few problems with the tests which I will go into below, but you can also look at each test individually and see that they are making the correct calls, and that the headers, and tests that are there are working correctly.

Exercise E - This is just the sum of the work located in this repository with this README explaining the work.

Issues with the tests,
1. I had to remove the authorization headers from the tests, so all tests will be run anonymously. I don't want to Post, Patch or Delete to the Facebook repository because it creates noise for other users, and GitHub already flagged my account for that, so I changed the tests so that they deliberately will not work when Posting, Patching, Puting, or Deleting to the repository.
2. Running anonymous tests on GitHub will quickly reach the data limit so I only have about 30 tests in total because after running a few and reaching the limit ALL tests will fail. So I had to compromise on the quality of some of the tests because I simply can't keep running them over and over to work out the perfect tests.

I think my work here is a good indication of what I can do if given some time with a project, and regret that I'm unable to cross all of the T's and dot all of the I's. If anyone is reviewing this, and would like to see more, or more detail in some of the tests, Please email me at dthomashtml@hotmail.com, and I'll try to get back to you with any changes that need to be made.

Thanks!

-Dustin Thomas

NEW - Added a new collection to the repository. Timestamp will use an API chain to pull the current CST from timezonedb.com and post it to both of my Github repositories. These tests all have the correct authorization headers (my own repositories) so they can be run as many times as needed. Check the results by going into the repository and looking at the issue comments.
