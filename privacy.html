document.addEventListener('DOMContentLoaded', function () {
  const form = document.getElementById('propertyForm');
  if (!form) return;

  form.addEventListener('submit', async function (e) {
    e.preventDefault();

    // Clear previous errors
    document.querySelectorAll('.form-error').forEach(el => el.classList.remove('show'));

    // Validate required fields
    let isValid = true;

    const requiredFields = [
      { id: 'propertyAddress', label: 'propertyAddress' },
      { id: 'fullName', label: 'fullName' },
    ];

    for (const field of requiredFields) {
      const el = document.getElementById(field.id);
      const errorEl = document.getElementById('error-' + field.id);

      if (!el.value.trim() || (el.type === 'checkbox' && !el.checked)) {
        if (errorEl) errorEl.classList.add('show');
        isValid = false;
      }
    }

    // Email format check (only if email is filled in)
    const emailEl = document.getElementById('email');
    const emailError = document.getElementById('error-email');
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (emailEl && emailEl.value.trim() && !emailRegex.test(emailEl.value.trim())) {
      emailError.classList.add('show');
      isValid = false;
    }

    if (!isValid) return;

    // Collect form data
    const formData = {
      submittedAt: new Date().toISOString(),
      property: {
        address: document.getElementById('propertyAddress').value,
        parcelSize: document.getElementById('parcelSize').value,
        zoning: document.getElementById('zoning').value,
        condition: document.getElementById('propertyCondition').value,
        motivation: document.getElementById('motivation').value,
      },
      contact: {
        fullName: document.getElementById('fullName').value,
        email: document.getElementById('email').value,
        phone: document.getElementById('phone').value,
      },
      consent: {
        smsOptIn: document.getElementById('smsConsent').checked,
        smsOptInTimestamp: document.getElementById('smsConsent').checked
          ? new Date().toISOString()
          : null,
        ageConfirm: document.getElementById('ageConfirm').checked,
        ageConfirmTimestamp: document.getElementById('ageConfirm').checked
          ? new Date().toISOString()
          : null,
        ipAddress: '',
        userAgent: navigator.userAgent,
      },
    };

    // Show loading state
    const submitBtn = form.querySelector('button[type="submit"]');
    const originalText = submitBtn.textContent;
    submitBtn.textContent = 'Submitting...';
    submitBtn.disabled = true;

    // Store to localStorage (for demo — replace with real endpoint)
    try {
      const submissions = JSON.parse(localStorage.getItem('bdlSubmissions') || '[]');
      submissions.push(formData);
      localStorage.setItem('bdlSubmissions', JSON.stringify(submissions));

      // Log for review
      console.log('New submission:', formData);

      // Show success
      form.style.display = 'none';
      document.getElementById('formSuccess').classList.add('show');

    } catch (err) {
      console.error('Submission error:', err);
      alert('Something went wrong. Please try again or contact us directly.');
      submitBtn.textContent = originalText;
      submitBtn.disabled = false;
    }
  });
});
