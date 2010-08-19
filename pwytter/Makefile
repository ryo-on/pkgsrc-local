# $NetBSD$
#

DISTNAME=	pwytter-0.8-src
PKGNAME=	${DISTNAME:S/-src//}
CATEGORIES=	www chat
MASTER_SITES=	http://pwytter.googlecode.com/files/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.pwytter.com/
COMMENT=	Pwytter is a standalone Twitter client
LICENSE=	gnu-gpl-v2

DEPENDS=	${PYPKGPREFIX}-qt4>=4.4:../../x11/py-qt4
DEPENDS+=	${PYPKGPREFIX}-Tk-[0-9]*:../../x11/py-Tk
DEPENDS+=	${PYPKGPREFIX}-imaging-[0-9]*:../../graphics/py-imaging
DEPENDS+=	${PYPKGPREFIX}-simplejson-[0-9]*:../../converters/py-simplejson

PKG_DESTDIR_SUPPORT=	user-destdir

DOCSDIR=	${PREFIX}/share/doc/${PKGBASE}
INSTALLATION_DIRS=	${DOCSDIR}

WRKSRC=			${WRKDIR}/pwytter-0.8
USE_PKGLOCALEDIR=	yes

SUBST_CLASSES+=			fix-paths
SUBST_STAGE.fix-paths=		pre-configure
SUBST_MESSAGE.fix-paths=	fixing pathes
SUBST_FILES.fix-paths=		setup.py
SUBST_SED.fix-paths=		-e 's,@DOCSDIR@,${DOCSDIR},g'

.include "../../lang/python/egg.mk"

#.include "../../x11/py-qt4/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
