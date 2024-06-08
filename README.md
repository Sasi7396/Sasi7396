<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Job Search</title>
  <!-- Bootstrap CSS -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css" integrity="sha384-xOolHFLEh07PJGoPkLv1IbcEPTNtaed2xpHsD9ESMhqIYd0nLMwNLD69Npy4HI+N" crossorigin="anonymous">
  <!-- Bootstrap Icons CSS -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
</head>

<body class="pl-5 bg-light">
  <div class="text-center pb-5">
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <i class="bi bi-circle-fill"></i>
      <a class="navbar-brand" href="#">nameless</a>
      <div class="collapse navbar-collapse " id="navbarSupportedContent ">
        <ul class="navbar-nav m-auto ">
          <li class="nav-item active ">
            <a class="nav-link " href="#">Start a search <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active ">
            <a class="nav-link" href="#">Jobs list<span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active ">
            <a class="nav-link" href="#">Salary estimate<span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item active ">
            <a class="nav-link" href="#">Pricing<span class="sr-only">(current)</span></a>
          </li>
        </ul>
        <form class="form-inline my-2 my-lg-0 ">
          <button class="btn btn-light btn btn-outline-dark" type="submit">Log in</button>
          <button class="btn btn-primary" type="submit">Sign up</button>
        </form>
      </div>
    </nav>
  </div>
  <div class="pb-5">
    <!-- Search Form -->
    <h1>Find your new job today</h1>
    <p>Thousands of jobs in the computer engineering and technology sectors are waiting for you.</p>
    <div>
      <form class="d-flex flex-row" id="searchForm">
        <div class="form-group mb-2 w-100">
          <input type="text" class="form-control" id="searchInput" placeholder="What position are you looking for ?">
        </div>
        <button type="submit" class="btn btn-primary mb-2">Search job</button>
      </form>
    </div>
  </div>
  <div class="container-fluid" id="jobList">
    <!-- Job Cards will be displayed here -->
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-3 bg-white">
          <h4>Filters</h4>
          <div>
            <p>Location</p>
            <div>
              <input type="radio" name="location" id="nearme" value="nearme">
              <label for="nearme">Near me</label>
            </div>
            <div>
              <input type="radio" name="location" id="remote" value="remote">
              <label for="remote">Remote job</label>
            </div>
            <div>
              <input type="radio" name="location" id="exact" value="exact">
              <label for="exact">Madrid</label>
            </div>
            <div>
              <input type="radio" name="location" id="within15" value="within15">
              <label for="within15">Brussels</label>
            </div>
            <div>
              <input type="radio" name="location" id="within30" value="within30">
              <label for="within30">United States</label>
            </div>
            <div>
              <input type="radio" name="location" id="within45" value="within45">
              <label for="within45">London</label>
            </div>
          </div>

          <div>
            <p>Salary</p>
            <button type="button" class="btn btn-outline-secondary">Hourly</button>
            <button type="button" class="btn btn-outline-secondary">Monthly</button>
            <button type="button" class="btn btn-outline-primary">Yearly</button>
            <div>
              <input type="radio" name="salary" id="any" value="any">
              <label for="any">Any</label>
            </div>
            <div>
              <input type="radio" name="salary" id="30k" value="30k">
              <label for="30k">>30k</label>
            </div>
            <div>
              <input type="radio" name="salary" id="50k" value="50k">
              <label for="50k">>50k</label>
            </div>
            <div>
              <input type="radio" name="salary" id="80k" value="80k">
              <label for="80k">>80k</label>
            </div>
            <div>
              <input type="radio" name="salary" id="100k" value="100k">
              <label for="100k">>100k</label>
            </div>
          </div>
          <div>
            <p>Date of posting</p>
            <div>
              <input type="radio" name="date" id="alltime" value="alltime">
              <label for="alltime">All time</label>
            </div>
            <div>
              <input type="radio" name="date" id="24hours" value="24hours">
              <label for="24hours">Last 24 hours</label>
            </div>
            <div>
              <input type="radio" name="date" id="3days" value="3days">
              <label for="3days">Last 3 days</label>
            </div>
            <div>
              <input type="radio" name="date" id="7days" value="7days">
              <label for="7days">Last 7 days</label>
            </div>
          </div>
          <div>
            <p>Work experience</p>
            <div>
              <input type="radio" name="experience" id="anyexp" value="anyexp">
              <label for="anyexp">Any experience</label>
            </div>
            <div>
              <input type="radio" name="experience" id="internship" value="internship">
              <label for="internship">Internship</label>
            </div>
            <div>
              <input type="radio" name="experience" id="remotework" value="remotework">
              <label for="remotework">Work remotely</label>
            </div>
          </div>
          <div>
            <p>Type of employment</p>
            <div>
              <input type="checkbox" id="fulltime" value="fulltime">
              <label for="fulltime">Full time </label>
            </div>
            <div>
              <input type="checkbox" id="temporary" value="temporary">
              <label for="temporary">Temporary </label>
            </div>
            <div>
              <input type="checkbox" id="parttime" value="parttime">
              <label for="parttime">Part-time </label>
            </div>
          </div>
        </div>
        <div class="col-md-6 bg-white">
         
          <div id="jobsContainer">
            
            <!-- Job Cards will be dynamically generated here -->
          </div>
        </div>
        <div class="col-md-3">
          <div class="card" style="width: 18rem;">
            <div class="card-body">
              <h5 class="card-title1"><i class="bi bi-envelope"></i>Email me for jobs</h5>
              <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
              <input type="email" name="" id="mail" class="w-100" placeholder="name@mail.com ">
              <button type="button" class="btn btn-primary btn-lg btn-block mt-2">Subscribe</button>
            </div>
          </div>
          <div class="card" style="width: 18rem;">
            <div class="card-body">
              <h5 class="card-title1"><i class="bi bi-rocket-takeoff-fill"></i>Get noticed</h5>
              <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
              <button type="button" class="btn btn-primary btn-lg btn-block">Upload Your resume</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- JavaScript -->
  <script>
    const jobs = [
      {
        company: 'Notion',
        title: 'Junior UI Designer',
        location: 'Madrid',
        type: 'Full time',
        salary: '30-32k',
        date: '1 day ago',
        description: 'Mollit in laborum tempor Lorem incididunt irure. Aute eu ex ad sunt. Pariatur sint culpa do incididunt eiusmod eiusmod culpa. laborum tempor Lorem incididunt.',
        logo: 'https://upload.wikimedia.org/wikipedia/commons/4/45/Notion_app_logo.png?20200221181224'
      },{
        company: 'Linear Company',
        title: 'Software Engineer',
        location: 'Brussels',
        type: 'Full time',
        salary: '50-52k',
        date: '1 day ago',
        description: 'Mollit in laborum tempor Lorem incididunt irure. Aute eu ex ad sunt. Pariatur sint culpa do incididunt eiusmod eiusmod culpa. laborum tempor Lorem incididunt.',
        logo: 'https://assets.production.skcript.com/cdn-cgi/image/width=230/featureos/site-assets/images/integrations/linear/linear.png'
      },
      {
        company: 'Spline Studio',
        title: 'Technical Support Engineer',
        location: 'United States',
        type: 'Full time',
        salary: '50-52k',
        date: '1 day ago',
        description: 'Mollit in laborum tempor Lorem incididunt irure. Aute eu ex ad sunt. Pariatur sint culpa do incididunt eiusmod eiusmod culpa. laborum tempor Lorem incididunt.',
        logo: 'https://cdn-1.webcatalog.io/catalog/spline/spline-icon-filled-256.png?v=1675594530708'
      },
      {
        company: 'Raycast corp',
        title: 'Product Engineer',
        location: 'London',
        type: 'Full time',
        salary: '40-42k',
        date: '2 days ago',
        description: 'Mollit in laborum tempor Lorem incididunt irure. Aute eu ex ad sunt. Pariatur sint culpa do incididunt eiusmod eiusmod culpa. laborum tempor Lorem incididunt.',
        logo: 'https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_9a487b4a4763a4c7feece5bf8f45f962/raycast.png'
      }
      
    ];

    function renderJobs(filteredJobs) {
      const jobsContainer = document.getElementById('jobsContainer');
      jobsContainer.innerHTML = '';
      filteredJobs.forEach(job => {
        const jobCard = `
          <div class="card mb-3" style="max-width: 700px;">
            <div class="row no-gutters">
              <div class="col-md-1 m-2">
                <img src="${job.logo}" alt="${job.company}" class="img-fluid">
              </div>
              <div class="col-md-8">
                <div class="card-body">
                  <p>${job.company}</p>
                  <h5 class="card-title">${job.title}</h5>
                  <i class="bi bi-geo-alt"></i><label>${job.location}</label>
                  <i class="bi bi-clock pl-2"></i><label>${job.type}</label>
                  <i class="bi bi-currency-dollar pl-2"></i><label>${job.salary}</label>
                  <i class="bi bi-calendar pl-2"></i><label>${job.date}</label>
                  <p class="card-text">${job.description}</p>
                </div>
              </div>
            </div>
          </div>
        `;
        jobsContainer.insertAdjacentHTML('beforeend', jobCard);
      });

      document.getElementById('jobCount').textContent = `${filteredJobs.length} Jobs`;
    }

    function filterJobs() {
      const searchInput = document.getElementById('searchInput').value.toLowerCase();
      const locationFilter = document.querySelector('input[name="location"]:checked')?.value || '';
      const salaryFilter = document.querySelector('input[name="salary"]:checked')?.value || '';
      const dateFilter = document.querySelector('input[name="date"]:checked')?.value || '';
      const experienceFilter = document.querySelector('input[name="experience"]:checked')?.value || '';
      const employmentFilters = Array.from(document.querySelectorAll('input[type="checkbox"]:checked')).map(cb => cb.value);

      const filteredJobs = jobs.filter(job => {
        const matchesSearch = job.title.toLowerCase().includes(searchInput) || job.description.toLowerCase().includes(searchInput);
        const matchesLocation = locationFilter ? job.location.toLowerCase().includes(locationFilter) : true;                 
        const matchesSalary = salaryFilter ? parseInt(job.salary.replace(/k/g, '')) >= parseInt(salaryFilter) : true;
        const matchesDate = dateFilter ? job.date.toLowerCase().includes(dateFilter) : true;
        const matchesExperience = experienceFilter ? job.description.toLowerCase().includes(experienceFilter) : true;
        const matchesEmployment = employmentFilters.length > 0 ? employmentFilters.includes(job.type.toLowerCase().replace(/\s+/g, '')) : true;

        return matchesSearch && matchesLocation && matchesSalary && matchesDate && matchesExperience && matchesEmployment;
      });

      renderJobs(filteredJobs);
    }

    document.getElementById('searchForm').addEventListener('submit', function (e) {
      e.preventDefault();
      filterJobs();
    });

    const filters = document.querySelectorAll('input[type="radio"], input[type="checkbox"]');
    filters.forEach(filter => {
      filter.addEventListener('change', filterJobs);
    });

    renderJobs(jobs); // Initial rendering of jobs
  </script>
</body>

</html>

