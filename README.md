# tests.navigation
describe('Navigation', () =>{
  it.skip('Courses',() =>{
    cy.visit('/user/login')

    cy.get('#normal_login_email')
      .type('snehoda@gmail.com')
    cy.get('#normal_login_password')
      .type('merdoc1981')
    cy.get('[type=submit]')
      .click()

    cy.get('[data-qa="topmenu-Courses"]')
      .click()

    cy.location('pathname')
      .should('include', '/course')
    cy.contains('Interactive Courses')
      .should('be.visible')
  })
  it.skip('Logo to main page',() =>{
    cy.visit('/user/login')

    cy.get('#normal_login_email')
      .type('snehoda@gmail.com')
    cy.get('#normal_login_password')
      .type('merdoc1981')
    cy.get('[type=submit]')
      .click()

    cy.get('[class="site-name text-nowrap"]')
      .click()

    cy.location('pathname')
      .should('include', '')
    cy.contains('Interactive learning')
      .should('be.visible')
    cy.contains('like an adventure')
      .should('be.visible')
  })

  it.skip('Interview questions',() =>{
    cy.visit('/user/login')

    cy.get('#normal_login_email')
      .type('snehoda@gmail.com')
    cy.get('#normal_login_password')
      .type('merdoc1981')
    cy.get('[type=submit]')
      .click()

    cy.get('[data-qa="topmenu-Interview Questions"]')
      .click()

    cy.location('pathname')
      .should('include', '/flash')
    cy.contains('Interview practice cards')
      .should('be.visible')
  })
  it.skip('Dairy',() =>{
    cy.visit('/user/login')

    cy.get('#normal_login_email')
      .type('snehoda@gmail.com')
    cy.get('#normal_login_password')
      .type('merdoc1981')
    cy.get('[type=submit]')
      .click()

    cy.get('[data-qa="topmenu-Diary"]')
      .click()

    cy.location('pathname')
      .should('include', '/diary')
    cy.contains('Daily reports')
      .should('be.visible')
  })
  it('Challenges',() =>{
    cy.visit('/user/login')

    cy.get('#normal_login_email')
      .type('snehoda@gmail.com')
    cy.get('#normal_login_password')
      .type('merdoc1981')
    cy.get('[type=submit]')
      .click()

    cy.get('[data-qa="topmenu-Challenges"]')
      .click()

    cy.location('pathname')
      .should('include', '/challenge')
    cy.contains('Challenges')
      .should('be.visible')
  })
})
