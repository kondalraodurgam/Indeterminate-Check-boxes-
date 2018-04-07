# Indeterminate-Check-boxes-
Checkbox inputs can only have two states: checked or unchecked. They can have any value, but they either submit that value (checked) or don't (unchecked) with a form submission. The default is unchecked. You can control that in HTML like this:
<ul>
			<li>
				<input type="checkbox" name="tall" id="tall">
				<label for="tall">Animals </label>
				<ul>
					<li>
						<input type="checkbox" name="tall-1" id="tall-1">
						<label for="tall-1">Tiger</label>
					</li>
					<li>
						<input type="checkbox" name="tall-2" id="tall-2">
						<label for="tall-2">Cat</label>
						<ul>
							<li>
								<input type="checkbox" name="tall-2-1" id="tall-2-1">
								<label for="tall-2-1">Dog</label>
							</li>
							<li>
								<input type="checkbox" name="tall-2-2" id="tall-2-2">
								<label for="tall-2-2">LeoPard</label>
							</li>
						</ul>
					</li>
					<li>
						<input type="checkbox" name="tall-3" id="tall-3">
						<label for="tall-3">Lion</label>
					</li>
				</ul>
			</li>
			<li>
				<input type="checkbox" name="short" id="short">
				<label for="short">Flowers </label>

				<ul>
					<li>
						<input type="checkbox" name="short-1" id="short-1">
						<label for="short-1">Rose:</label>
						</li>
					<li>
						<input type="checkbox" name="short-2" id="short-2">
						<label for="short-2">Tulips:</label>
					</li>
					<li>
						<input type="checkbox" name="short-3" id="short-3">
						<label for="short-3">Orchids:</label>
					</li>
				</ul>
			</li>
		</ul>
    
      Visually, there are actually three states a checkbox can be in: checked, unchecked, or indeterminate. They look like this:


      Here are some things to know about indeterminate checkboxes:

      You can't make a checkbox indeterminate through HTML. There is no indeterminate attribute. It is a property of checkboxes though, which you can change via JavaScript.

      var checkbox = document.getElementById("some-checkbox");
      checkbox.indeterminate = true;
      or jQuery style:

      $("#some-checkbox").prop("indeterminate", true); // prop is jQuery 1.6+
      The indeterminate state is visual only. The checkbox is still either checked or unchecked as a state. That means the visual indeterminate state masks the real value of the checkbox, so that better make sense in your UI!

      Like the checkboxes themselves, indeterminate state looks different in different browsers. Here's Opera 11.50 on Mac:


      #Use Case
      The reason I'm writing this at all is because I just had a use case come up for this state: nested checkboxes. Each checkbox may have child checkboxes. If all those children are checked, it may be checked. If none are checked, it is unchecked. If some of them are checked, then it's in an indeterminate state (in this case symbolically meaning "partially" checked).

