    <div class="col-12 col-md-4 mb-3">
       <div class="team team-summary">
         <div class="team-image">
             <img alt="{{ team.title }}" class="img-fluid mb-2" src="{{ person.photo | relative_url }}" />
         </div>
         <div class="team-meta">
         {% if person.website and person.website != blank %}
            <h2><a href="{{person.website}}">{{person.name}}</a></h2>
	 {% else %}
            <h2 class="team-name">{{person.name}}</h2>
         {% endif %}
         <p class="team-description"><i>{{person.title}}</i></p>
         </div>
       </div>
     </div>

