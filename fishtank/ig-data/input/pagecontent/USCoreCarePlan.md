[Previous Page - US Core AllergyIntolerance](USCoreAllergyIntolerance.html)

Where a Health Plan has access to Care Plan information for a member they **SHALL** make the information available using the [US Core CarePlan](http://hl7.org/fhir/us/core/StructureDefinition-us-core-careplan.html) resource.

The essential fields to be provided in the CarePlan  resource are:

| R4 Hierarchical Name            | R4 Name  | Flags | Card. | Type                               |
|---------------------------------|----------|-------|-------|------------------------------------|
| CarePlan                        | CarePlan | I     | 0..*  |                                    |
| CarePlan.id                     | id       |      | 0..1  | id                                 |
| CarePlan.text                   | text     | S     | 1..1  | Narrative                          |
| CarePlan.text.status            | status   | S     | 1..1  | code                               |
| CarePlan.text.div               | div      | I     | 1..1  | xhtml                              |
| CarePlan.status                 | status   | ?!S  | 1..1  | code                               |
| CarePlan.intent                 | intent   | ?!S  | 1..1  | code                               |
| CarePlan.category               | category | SI   | 1..*  | CodeableConcept                    |
| CarePlan.subject                | subject  | S    | 1..1  | Reference(US Core Patient Profile) |
| CarePlan.activity.detail.status | status   | ?!    | 1..1  | code                               |

#### Example CarePlan Resource

An example mapping of a CarePlan for a colonoscopy is shown below:

<pre>
{
  "resourceType" : "CarePlan",
  "id" : "colonoscopy",
  "meta" : {
    "profile" : [
      "http://hl7.org/fhir/us/core/StructureDefinition/us-core-careplan"
    ]
  },
  "text" : {
    "status" : "additional",
				"div" : "<div xmlns=\"http://www.w3.org/1999/xhtml\">      
				            <strong>Assessment</strong>
				            <ol><li>Recurrent GI bleed of unknown etiology; hypotension perhaps secondary to this but as likely secondary to polypharmacy.</li>
										       <li>Acute on chronic anemia secondary to #1.</li>
													 <li>Azotemia, acute renal failure with volume loss secondary to #1.</li>
													 <li>Hyperkalemia secondary to #3 and on ACE and K+ supplement.</li>
													 <li>Other chronic diagnoses as noted above, currently stable.</li>
										</ol>
										<table>
										      <thead>
													    <tr>
															     <th>Planned Activity</th>
																	 <th>Planned Date</th>
														 </tr>
												 </thead>
												<tbody>
												    <tr>
														     <td>Colonoscopy</td>
																 <td>April 21, 2000</td>
													</tr>
										 </tbody>
							</table>
							</div>"
  },
  "status" : "active",
  "intent" : "order",
  "category" : [
    {
      "coding" : [
        {
          "system" : "http://hl7.org/fhir/us/core/CodeSystem/careplan-category",
          "code" : "assess-plan"
        }
      ]
    }
  ],
  "subject" : {
    "reference" : "Patient/example",
    "display" : "Amy Shaw"
  }
}
</pre>



[Next Page - US Core CareTeam](USCoreCareTeam.html)